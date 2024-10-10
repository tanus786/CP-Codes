import java.util.Arrays;

public class LongestIncreasingSubsequence {

    // Function to return the length of the longest increasing subsequence
    public static int lengthOfLIS(int[] nums) {
        if (nums == null || nums.length == 0) {
            return 0;
        }

        int[] dp = new int[nums.length];
        int len = 0;

        for (int num : nums) {
            // Use binary search to find the index of the current number in the dp array
            int i = Arrays.binarySearch(dp, 0, len, num);

            // If not found, binarySearch returns (-(insertion point) - 1)
            if (i < 0) {
                i = -(i + 1);
            }

            // Place the current number at the found index
            dp[i] = num;

            // If the number is placed at the end, increase the length of LIS
            if (i == len) {
                len++;
            }
        }

        return len;
    }

    // Driver code
    public static void main(String[] args) {
        int[] nums = {10, 9, 2, 5, 3, 7, 101, 18};
        System.out.println("Length of Longest Increasing Subsequence: " + lengthOfLIS(nums));
    }
}
