myfunc() {
    echo "hello $1"
}
# Same as above (alternate syntax)
function myfunc() {
    echo "hello $1"
}
myfunc "John"


myfunc() {
    local myresult='some value'
    echo $myresult
}
result="$(myfunc)"

name="John"
echo ${name}
echo ${name/J/j}    #=> "john" (substitution)
echo ${name:0:2}    #=> "Jo" (slicing)
echo ${name::2}     #=> "Jo" (slicing)
echo ${name::-1}    #=> "Joh" (slicing)
echo ${name:(-1)}   #=> "n" (slicing from right)
echo ${name:(-2):1} #=> "h" (slicing from right)
echo ${food:-Cake}  #=> $food or "Cake"
length=2
echo ${name:0:length}  #=> "Jo"
