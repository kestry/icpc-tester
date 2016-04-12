#!/bin/bash
valid=true

for i in $( ls *.in); do
	output=$(./$1 < $i)
	name=$(echo $i | cut -d "." -f1)
	ans=$(cat $name.ans)
	if [ "$output" != "$ans" ]; then
		valid=false
		printf "FAILED: $name\n"
		printf "$i:\n$(cat $i)\n"
		printf "Your output:\n$output\n"
		printf "Answer:\n$ans\n\n"
	fi
done

if [ "$valid" = true ]; then
	printf "All cases passed\n"
fi
