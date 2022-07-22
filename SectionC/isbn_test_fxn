def isbn_test(input):

  # convert input string to list of characters
  input_list = []
  for el in input:
    input_list.append(el)
  
  # replace last value, if it is an 'X', with '10'
  if input_list[-1] == 'X':
      input_list[-1] = 10
  
  # convert all elements of list to integer
  for ind, el in enumerate(input_list):
    input_list[ind] = int(input_list[ind])

  # check if ISBN-10
  if len(input_list) == 10:

    # instantiate validity-check product list
    isbn10_prod = [10,9,8,7,6,5,4,3,2,1]
    
    # instantiate empty list
    prod_result = []

    # calculate validity product of each value of ISBN-10
    for ind, no in enumerate(input_list):
      prod_result.append(input_list[ind] * isbn10_prod[ind])
    
    # check whether sum of validity products divisible by 11
    if sum(prod_result) % 11 == 0:

      # insert 678 at front of ISBN-10
      input_list = [6,7,8] + input_list
      
      # convert list of integers to strings and concatenate
      output = []
      for el in input_list:
        output.append(str(el))
      output = "".join(output)

      return output

    # return "Invalid" if ISBN-10 does not meet above validity criteria
    else:
      return "Invalid"

  # handle ISBN-13
  elif len(input_list) == 13:
    
    # instantiate validity-check product list
    isbn13_prod = [1,3,1,3,1,3,1,3,1,3,1,3,1]

    # instantiate empty list
    prod_result = []

    # calculate validity product of each value of ISBN-13
    for ind, no in enumerate(input_list):
      prod_result.append(input_list[ind] * isbn13_prod[ind])

    # check whether sum of validity products divisible by 11
    if sum(prod_result) % 10 == 0:
      return "Valid"
    else:
      return "Invalid"
