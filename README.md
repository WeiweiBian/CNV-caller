# CNV-caller



## 1. Get read count:

sed -e 's/:umi:/\t/' -e 's:/2::' on-target.cnt | cut -f 4,5,11 > __cnt

sort --parallel=4 -u __cnt > __cnt.s

cut -f 1,2 __cnt.s | uniq -c | gawk '{print $2,$3,$1}' > __cnt.s.n

## 2. Merge panel info



## 3. Normalisation 
-- Total number of reads

-- Primer efficiency (panel specific)


## 4. Calculate P value 


## 5. Visualization
