# Prova-Final---Tarcisio
# a) e = ( a – ( b – c ) + f )
.text
addi $s0, $zero, 10
addi $s1, $zero, 2
addi $s2, $zero, 5

sub $s4, $s1, $s2
sub $s4, $s0, $s4
add $s4, $s4, $s5
# b) f = e – (a – b ) + ( b – c )

.text

addi $s0, $zero, 15
addi $s1, $zero, 10
addi $s2, $zero, 5
addi $s4, $zero, 10

sub $t1, $s0, $s1
sub $t1, $s4, $t1
sub $t2, $s1, $s2
add $s5, $t1, $t2


# c) a = b[15] – c;
.data

b: .word 1, 2, 3, 8, 55, 6, 65, 8, 9, 10, 11, 12, 18, 14, 15, 16 # criação do vetor
.text
la $s1, b

addi $s2, $zero, 5
addi $t1, $zero, 15

add $t2, $t1, $t1
add $t2, $t2,$t2
add $t2, $t2, $s1

lw $t3, 0($t2)

sub $s0, $t3, $s2

# d) a[10] = b – c;

.data 

a: .word  1, 21, 3, 4, 25, 6, 17, 8, 9, 10, 11

.text

la $s0, a

addi $s1, $zero, 10
addi $s2, $zero, 64

sub $t2, $s1, $s2

sw $t2, 10($s0)



