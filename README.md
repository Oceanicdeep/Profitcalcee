def calculate_required_price(investment_cost, desired_profit, num_shares):
    """
    Calculate the required price per share to achieve the desired profit.
    
    Parameters:
    - investment_cost (float): The total cost of investment.
    - desired_profit (float): The profit you wish to earn.
    - num_shares (float): The number of shares purchased.
    
    Returns:
    - float: The required stock price per share.
    """
    total_target_value = investment_cost + desired_profit
    required_price = total_target_value / num_shares
    return required_price

def main():
    try:
        investment_cost = float(input("Enter your total investment cost (₹): "))
        desired_profit = float(input("Enter your desired profit (₹): "))
        num_shares = float(input("Enter the number of shares: "))
        
        if num_shares == 0:
            print("Number of shares cannot be zero.")
            return
        
        required_price = calculate_required_price(investment_cost, desired_profit, num_shares)
        print(f"\nTo earn a profit of ₹{desired_profit:.2f} on an investment of ₹{investment_cost:.2f} for {int(num_shares)} shares,")
        print(f"the stock price needs to reach: ₹{required_price:.2f} per share.")
    
    except ValueError:
        print("Invalid input. Please ensure you enter numeric values.")

if __name__ == "__main__":
    main()
