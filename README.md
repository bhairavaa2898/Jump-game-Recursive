# Jump-game-Recursive
class Solution {
    public boolean canJump(int[] nums) {
        return helper(nums, 0);
    }
    private boolean helper(int[] nums, int index) {
        if (index >= nums.length - 1) {
            return true;
        }
        int maxJump = nums[index];
        for (int jump = 1; jump <= maxJump; jump++) {
            if (helper(nums, index + jump)) {
                return true;
            }
        }
        return false;
    }
}
