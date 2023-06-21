# Supermarket-Data-Analysis-Using-Jupyter-Notebook
Data analysis using jupyter notebook of supermarket data. 
<!--  -->
For histogram 




<!--  -->

<!--  -->
For bar graph

payment_mode_quantity = sales_data.groupby('Payment Mode')['Quantity'].sum()
payment_mode_quantity.plot(kind='bar')
plt.xlabel('Payment Mode')
plt.ylabel('Quantity')
plt.title('Payment Mode VS Quantity')
plt.show()
<!--  -->

<!--  -->
For pie chart

category_counts = sales_data['Category'].value_counts()
plt.pie(category_counts.values, labels=category_counts.index, autopct='%1.1f%%')
plt.title('Category Distribution')
plt.show()




<!--  -->
For linear graph

subcategory_count = sales_data.groupby('Sub-Category').size()
plt.plot(subcategory_count.index, subcategory_count.values, marker='o')

# Set the labels and title
plt.xlabel('Sub-Category')
plt.ylabel('Count')
plt.title('Count of Sub-Categories')

# Rotate x-axis labels if needed
plt.xticks(rotation=90)

# Display the plot
plt.show()


