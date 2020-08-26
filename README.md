# leetcode 1351 - Count Negative Numbers in a Sorted Matrix

## C#
```C#
public static int CountNegatives(int[][] grid)
{
    int count = 0;
    int rowLen = grid.Length;
    int colLen = grid[0].Length;            
    for(int i = 0; i < colLen; i++)
    {
        for(int j = 0; j < rowLen; j++)
        {
            if(grid[j][i] < 0)
            {
                count += (colLen - i) * (rowLen - j);
                rowLen = j;
            }
        }
    }
    return count;
}
```
