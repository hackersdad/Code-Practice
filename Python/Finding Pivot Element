# The pivot index is the index where the sum of all the numbers strictly to the left of the index is equal to the sum of all the numbers strictly to the index's right.

# If the index is on the left edge of the array, then the left sum is 0 because there are no elements to the left. This also applies to the right edge of the array.

# logic 
# Similar to the concept of binary search 
# or saying realistically the concept of weighing using 'taraazuu' 
# when weight is more on one side, either add something on the lesser side
# or remove something from the higher side

# Implementing same in binary search style
# go to middle take sum of left array and right array
# if they are same then you found the pivot element 
# if left is greater move pivot to left else move it to right


def find_pivot(nums):
    
    start = 0
    end = len(nums) -1
    mid = int((start+end)/2)
    pivot = ""
    break_flag = False 
    while not pivot:
        behind_sum = sum(nums[:mid])
        forward_sum = sum(nums[mid+1:])
        print("mid -> "+str(mid)+" behind : "+str(behind_sum)+" forwaard : "+str(forward_sum))
        
        if(behind_sum == forward_sum):
            pivot = mid
            break
        
        if(mid == start or mid == end):
            break;
        
        if(behind_sum > forward_sum):  
            
            end = mid
            mid = int((start+end)/2)
        elif(behind_sum < forward_sum):
            start = mid
            mid = int((start+end)/2)
    
    if(pivot != ""):
        return pivot
    else:
        return -1


nums = [1,7,3,6,5,6]
find_pivot(nums)
