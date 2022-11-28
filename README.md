# Sort-Colors
class Solution:
    def sortColors(self, nums: List[int]) -> None:
        low=0
        mid=0
        high=len(nums)-1
        while (mid<=high):
            if(nums[mid]==0):
                nums[mid]=nums[low]
                nums[low]=0
                low+=1
                mid+=1
            elif(nums[mid]==2):
                nums[mid]=nums[high]
                nums[high]=2
                high-=1
            elif(nums[mid]==1):
                mid+=1
