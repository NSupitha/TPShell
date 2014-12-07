TPShell
=======

for i in $(find . -type f)
do
 	
        count=$(cat $i | wc -l)
 
       if [ $count -gt 10 ]
            then 
                  echo "$i;$count"
                  x=$( echo $i | sed 's/f/g/g')
            mv $i $x
fi

done  
