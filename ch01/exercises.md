## Excercise 1.1

   10
   ;; 10

   (+ 5 3 4)
   ;; 12

   (- 9 1)
   ;; 8

   (/ 6 2)
   ;; 3

   (+ (* 2 4) (- 4 6))
   ;; 6

   (define a 3)
   ;; a

   (define b (+ a 1))
   ;; b

   (+ a b (* a b))
   ;; 19

   (= a b)
   ;; #f

   (if (and (> b a) (< b (* a b)))
       b
       a)
   ;; 4

   (cond ((= a 4) 6)
         ((= b 4) (+ 6 7 a))
         (else 25))
   ;; 16

   (+ 2 (if (> b a) b a))
   ;; 6

   (* (cond ((> a b) a)
            ((< a b) b)
            (else -1))
      (+ a 1))
   ;; 16

## Exercise 1.2

   (/ (+ 5 4 (- 2 (- 3 (+ 6 (/ 4 5)))))
      (* 3 (- 6 2) (- 2 7))))
   ;; (/ (+ 5 4 ()) (* 3 4 -5)

## Exercise 1.3

   (define (square x) (* x x))
   (define (sum-of-squares a b)
           (+ (square a) (square b)))
   (define (sum-of-larger-squares a b c)
           (cond ((and (> a b) (> b c)) (sum-of-squares a b))
                 ((and (> b a) (> c a)) (sum-of-squares b c))
                 ((and (> b a) (> a c)) (sum-of-squares b a))
                 ((and (> a b) (> c b)) (sum-of-squares a c))
                 (else -1)))
   ;;

