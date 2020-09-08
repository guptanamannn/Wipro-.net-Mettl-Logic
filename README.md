# Wipro-dotNet-Mettl-Logic

________________________________________________________________________
*Convet to String: str.ToString();

*String Length: str.Length;

*Even: input1%2==0

*Odd: input1%2!=0

*Last Degit: input1%10

*Second Last Degit: input1=input1/10; | input1%10;

*Exact Multiple: input1%input2==0

*Prime Number: 
	int cnt=0;
        for(int i=1;i<=input1;i++){
            if(input1%i==0){
                cnt++;
            }
        }

*Factorial:
	int fact=1;
        for(int i=1;i<=input1;i++){
            fact=fact*i;
        }

*Fibonacci:
	for(int i=3;i<=input1;i++){
            c=a+b;
            a=b;
            b=c;
        }

*nth Prime: 
	for(i=2;i>0;i++){
            flag=0;
            for(j=2;j<i;j++){
                if(i%j==0){
                    flag=1;
                    break;
                }
            }
            if(flag==0){
                cnt++;
            }
            if(cnt==input1){
                return i;
                break;
            }
        }

*All Digits Count:
*Method1:
	 int cnt=0;
        while(input1>0){
            int r= input1%10;
            cnt++;
            input1=input1/10;
        }

*Method2:
	int d= input1.ToString().Length;
        return d;

*Unique Digits Count:
	int temp;
        int cnt=0;
        int [] h=new int [10];
        while(input1>0){
            
            temp=input1%10;
            h[temp]++;
            input1=input1/10;

        }
        for(int i=0;i<10;i++){
            if(h[i]>0){
                cnt++;
            }
        }

        return cnt;

*Non Repeted Digits:
	int [] h=new int [10];
        int cnt=0;
        while(input1>0){
            int temp=input1%10;
            h[temp]++;
            input1=input1/10;
        }
        for(int i=0;i<10;i++){
            if(h[i]==1){
                cnt++;
            }
        }

        return cnt;

*Digit Sum:
	while(b){
			
			while(input1>0){
			int r=input1%10;
			sum=sum+r;
			input1=input1/10;
			}
			if(sum<10){
			b=false;
			}
			else{
			input1=sum;
			sum=0;
			}
		}
		if(x<0){
			sum=(-1)*sum;
		}


*Even Digit Sum:
	 int sum=0;
        while(input1>0){
            int r=input1%10;
            if(r%2==0){
                sum=sum+r;
            }
            input1=input1/10;
        }
        return sum;

*Odd Digit Sum:
	int sum=0;
        while(input1>0){
            int r=input1%10;
            if(r%2!=0){
                sum=sum+r;
            }
            input1=input1/10;
        }
        return sum;

*Sum Of Even Odd:
	int sum=0;
        while(input1>0){
            int r=input1%10;
            if(input2=="odd"){
                if(r%2!=0){
                sum=sum+r;
                }
            }
            if(input2=="even"){
                if(r%2==0){
                sum=sum+r;
                }

            }
            
            input1=input1/10;
        }
        return sum;

*Palindrome Number:
	int temp=input1;
        int rev=0;
        while(input1>0)
        {
            rev=rev*10+input1%10;
            input1/=10;
            }
            if(rev!=temp)
            return 1;
            else
            return 2;
        }

*Is Palindrome Possible:
	int []a= new int [10];
        while(input1>0){
            int r=input1%10;
            a[r]++;
            input1= input1/10;

        }
        int odd=0;
        for(int i=0;i<10;i++)
        {
            if(a[i]==1){
                odd++;
            }
            if(odd>1){
                return 1;
            }
        }
        return 2;

*Pin:
	 //Write code here
        int pin;
        int unitone;
        int tens;
        int hun;

        int a=input1%10;
        int b=input2%10;
        int c=input3%10;

        if(a<b&a<c){
            unitone=a;
        }
        else if(b<c & b<a){
            unitone=b;
        }
        else{
            unitone=c;
        }
        int aa=(input1/10)%10;
        int bb=(input2/10)%10;
        int cc=(input3/10)%10;

        if(aa<bb&aa<cc){
            tens=aa;
        }
        else if(bb<cc & bb<aa){
            tens=bb;
        }
        else{
            tens=cc;
        }
        int aaa=(input1/100)%10;
        int bbb=(input2/100)%10;
        int ccc=(input3/100)%10;

        if(aaa<bbb&aaa<ccc){
            hun=aaa;
        }
        else if(bbb<ccc & bbb<aaa){
            hun=bbb;
        }
        else{
            hun=ccc;
        }
       

      int u1=input1%10,u2=input2%10,u3=input3%10;
        int t1=(input1/10)%10,t2=(input2/10)%10,t3=(input3/10)%10;
        int h1=input1/100,h2=input2/100,h3=input3/100;

        int th=Math.Max(u1,Math.Max(u2,Math.Max(u3,Math.Max(t1,Math.Max(t2,Math.Max(t3,Math.Max(h1,Math.Max(h2,h3))))))));

        return th*1000+hun*100+tens*10+unitone;

*Weight Hill Pattern:
	int i,j,sum=0;
        for( i=0;i<input1;i++){
            for(j=0;j<=i;j++){
                sum = sum+input2;
                
                
            }
            input2=input2+input3;
                
           
        }
        return sum;

*Second Word in UpperCase:
	string [] s= input1.Split(' ');
        if(s.Length==1){
            return "LESS";
        }
        string s1=s[1];
        s1=s1.ToUpper();
        return s1;

*Palindrome String:
	input1=input1.ToLower();
        char [] arr=input1.ToCharArray();
        Array.Reverse(arr);
        string s = new string(arr);

        if(s==input1){
            return 2;
        } 
        else{
            return 1;
        }


*String Weight:
	String small="abcdefghijklmnopqrstuvwxyz";
        int sum=0;
        int i;
        input1=input1.ToLower();
        
        for(i=0;i<input1.Length;i++){
            char c=input1[i];
            if(input2==0){
                
                int index=small.IndexOf(c);
                if(c!='a'&&c!='e'&&c!='i'&&c!='o'&&c!='u'){
                    if(index>=0){
                        sum=sum+index+1;
                    }
                    else{
                        sum=sum+0;
                    }
                }
                

            }
            else{
                int index=small.IndexOf(c);
                if(index>=0){
                    sum=sum+index+1;
                }
                else{
                    sum=sum+0;
                }
            }
            

        }
        return sum;


*Most Frequent Digit:
	int []h=new int [10];
        int index=0,max=-1;
        int i;
        if(input1==0&&input2==0&&input3==0&&input4==0){
            return 0;
        }
        if(input1==0){
            h[0]++;
        }
        if(input2==0){
            h[0]++;
        }
        if(input3==0){
            h[0]++;
        }
        if(input4==0){
            h[0]++;
        }
        while(input1>0)
        {
            h[input1%10]++;
            input1/=10;
        }
        while(input2>0)
        {
            h[input2%10]++;
            input2/=10;
        }
        while(input3>0)
        {
            h[input3%10]++;
            input3/=10;
        }
        while(input4>0)
        {
            h[input4%10]++;
            input4/=10;
        }
        
        for(i=0;i<10;i++){
            if(max<=h[i])
            {
                max=h[i];
                index=i;
            }
        }
        return index;








