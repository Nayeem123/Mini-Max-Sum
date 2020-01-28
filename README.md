# Mini-Max-Sum
Given five positive integers, find the minimum and maximum values that can be calculated by summing exactly four of the five integers. Then print the respective minimum and maximum values as a single line of two space-separated long integers.


static void miniMaxSum(int[] arr) {
        int len=arr.length;
            long sum[] = new long[len];
            for(int i=0;i<arr.length;i++)
            {
                for(int j=0;j<arr.length;j++)
                {
                    if(i == j)
                    {
                        continue;
                    }
                    sum[i] +=arr[j];
                }
            }
            
            Arrays.sort(sum);
            System.out.print(sum[0]+" "+sum[len-1]);
    }
