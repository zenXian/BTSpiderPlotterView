BTSpiderPlotterView
===================

![sample](/Gifs/spiderview.gif)

This is a view for you to use as-is or modify the source. The view comes loaded with the ability to:

1. Plot a spider web graph from a data dictionary to fit the view given  
2. Automatic resizes  
3. Minor customization on color and plotting method  
4. It should just work! like magic! 

**Background:**  
There are many ways to present your data, this is one of the visualization method that I use in my app. I think it has a lot of application to it, thus wanted to share with you all.   

**Implementation:**  
The view is a subclass of a UIView. It determines the best fit size for the given frame (ie, the min of width and height). From there, it calculates the relative points where each plot should end up at and store in an array. At the drawRect, it plots all the points from the array using `CGContext`. 

**How to use:**

1. Import `BTSpiderPlotterView.h`  
2. Create an `NSDictionary` containing the value you would like to plot. Key will hold the label and value will hold number (eg, `@{@"First": @"5", @"Second": @"6", @"Third": @"3"}`).
3. Create an instance of spiderPlotterView with `- (id)initWithFrame:(CGRect)frame valueDictionary:(NSDictionary *)valueDictionary`  
4. Add the view as subview per usual.
5. Profit! unless, you want to customize, feel free to change any of the four public variables as it automatically change the plot


Please view example project to get the idea of how to implement. 
* please have at least 3 key-pair value dictionary for obvious reasons

Animation code was contributed by Cdtschange - https://github.com/cdtschange

----

**Copyright 2014 Byte**

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
