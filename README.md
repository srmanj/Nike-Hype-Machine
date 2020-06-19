# Reselling Off-White Sneakers - The Nike Hype Machine

This blog shows my work on a personal project where I use sneaker sales data from Stock X and try to quantify the behavior of “**Hype**” as a metric.
Medium - https://medium.com/@sriharsha.m3/reselling-off-white-sneakers-a-look-into-the-nikes-hype-machine-7544459f4c2

# **🔥Hype — An indirect form of marketing with the goal of up-keeping or improving brand value through the sale of products that are coveted by brand loyalists & consumers**

These coveted products are then traded at a steep marked up price, sometimes at preposterous values. This in turn creates more publicity and associates the brand with that image of having a really high value.

Although originally released by Nike, these hyped products are traded among consumers for a considerable profit. Platforms like GOAT and Stock X help Nike fan the flames of hype by providing a trusted platform for re-sale of coveted sneakers.

Limited supply is key to feed and help thrive such mini-economies of traded sneakers. Celebrity collaborations is another way to do it. In my initial research, I have come across people who consider sneakers as a legitimate investment vehicle for their savings.

Having known the above, I was interested in analytically defining Hype, or at least be able to explain its behavior across products

# **Data**

The data I used comes from the [Stock X Data Contest](https://stockx.com/news/the-2019-data-contest/) from 2019. It consists of a random sample for X% of daily sales of all Off-White x Nike and Yeezy 350 sales from between 9/1/2017 (the month that Off-White first debuted “The Ten” collection) and the present. There are 99,956 total sales in the data set; 27,794 Off-White sales, and 72,162 Yeezy sales.

The fields consist of — Order Date, Brand, Sneaker Name, Sale Price ($), Retail Price ($), Release Date, Shoe Size, and Buyer State

# **Hype — as a Metric**

From the available data, we can quantify the hype using 2 things —

1. Markup rate(%) from the original retail price
2. Number of weeks the product sells at an above average markup rate

For simplicity, let’s say a product is hyped if it sells at a markup of 200% i.e. twice its retail price.

Since this is re-sale data from a secondary market external to Nike, We cannot look at it the same way we look at sales data. The market in this case is not exactly driven by supply & demand in the traditional sense. If a certain product is available, customers are willing to buy with little regard to the cost.

Hence, looking at units sold or dollar sales would not be suitable, Instead looking at the markup rate — i.e. the percentage change from the retail price would make more sense.

We can visualize the change in markup rate or “hype” in a graph that is centered at the release week. Week 0 in the figure below shows the release week.

Behavior of Markup Rate against Number of weeks from Official Release

![https://miro.medium.com/max/1499/1*ZrylcnVi2pXPQ8Phaz9iAw.png](https://miro.medium.com/max/1499/1*ZrylcnVi2pXPQ8Phaz9iAw.png)

As can be seen here, Stock X allows people to start selling sneakers **before their release.**It also seems likely that hype is correlated with the **heat level** of the sneaker. A key observation/hypothesis one can make from the above image is that there are 2 main categories of hype —

**🔥Bucket 1 — High Heat Products — More Hype**

These products generally start out with a high pre-release markup. Then see decay after the release when the market is saturated with the product but, eventually appreciate in value over time and exceed release week markup rates. (The products in this category are traded for periods after they are released). *It seems like they almost follow a swoosh-like trend.*

High Heat Products and their hype behavior against Number of weeks from release

![https://miro.medium.com/max/1285/1*11-DWU4y0W0SnZaGC62m5Q.png](https://miro.medium.com/max/1285/1*11-DWU4y0W0SnZaGC62m5Q.png)

**🔥Bucket 2 — Medium-Low Heat Products — Lower Hype**

These products in most cases see their highest markup rates before and during the release week but, depreciate a couple of weeks after the release. (The products in this category are not traded for long periods of time)

![https://miro.medium.com/max/1557/1*FmqfAXUX99IfVKbfpMi5Vw.png](https://miro.medium.com/max/1557/1*FmqfAXUX99IfVKbfpMi5Vw.png)

Now, looking at the overall hype behavior across all the products — We can observe a common decay after release and increase in hype after that.

![https://miro.medium.com/max/1499/1*1UF7dFKGdcSo3175sOJGWg.png](https://miro.medium.com/max/1499/1*1UF7dFKGdcSo3175sOJGWg.png)

# **Insights**

# **💡Insight 1- The worst hype observed for a product on average is the first 15 weeks after the release**

So, If you’re someone who’s looking to sell an Off-White sneaker, you stand to make more of a profit if you either sell before the release or wait till week 20.

# **💡 Insight 2- Identifying the heat level of the sneaker informs the best time to sell**

If your product belongs to the High Heat category, you are better off to hold on to your product until week 20. If not, you are likely to see the most profit for your product pre-release.

[https://miro.medium.com/max/750/0*pJqVW1e_w8OlmpLj.png](https://miro.medium.com/max/750/0*pJqVW1e_w8OlmpLj.png)

Air Jordan 1’s Off-White Retro High Chicago

This simple exercise is a small window into the fandom Nike has curated over the years.

Although an obvious choice, one product that caught my eye and say the most markup rate in this data set were the Air Jordan 1’s Off-White Retro High Chicago

If I had more access to the data, I would —

- Build a model that could predict the hype of a product based on product attributes (including heat level)
- Analyze the differences in hype levels with regard to collaborations
- Model a baseline that would inform impact from a product hype to Nike’s baseline with the release of each new product

🐱‍👤With that, I’d like to thank you for taking the time to read this article all the way. If you wish to view the code for the same, Find it [here](https://github.com/srmanj/Nike-Hype-Machine/blob/master/Nike-off-white-hype-measurement.ipynb)
