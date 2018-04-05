---
UID: NN:tuner.IBDAComparable
title: IBDAComparable
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibdacomparable.htm
old-project: mstv
ms.assetid: 6f582ae2-d8c6-4d85-a01f-e98c6ee16021
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDAComparable, IBDAComparable interface [Microsoft TV Technologies], IBDAComparable interface [Microsoft TV Technologies], described, IBDAComparableInterface, mstv.ibdacomparable, tuner/IBDAComparable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IBDAComparable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IBDAComparable interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IBDAComparable</b> interface compares two objects to determine whether they contain the same or equivalent tuning information. DirectShow supports this interface in its implementation of the <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a>, <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a>, <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a>, <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a>, and <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> base interfaces and in the derived interfaces that inherit from these base interfaces. An application can query a component, component-type, tune-request, locator, or tuning-space object for an <b>IBDAComparable</b> interface that it can use to compare the tuning properties of the object to those of another object of the same type.

To support comparisons of the tuning properties of similar objects, two of the methods in this interface compare the property values directly. The remaining methods generate 64-bit CRC values from the property values for each object that the caller can compare to determine whether the objects have the same or equivalent properties.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDAComparable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDAComparable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDAComparable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/132c326e-053c-41be-b0fd-bea484fb0acd">CompareEquivalent</a>
</td>
<td align="left" width="63%">
Compares two objects to determine whether they contain equivalent tuning information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65053d86-4c8c-4c68-90a6-118454cf2eb1">CompareExact</a>
</td>
<td align="left" width="63%">
Compares two objects to determine whether they contain the same tuning information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31f52445-a4f5-40f5-ad55-30f3b43b1528">HashEquivalent</a>
</td>
<td align="left" width="63%">
Generates a hash code for a subset of the tuning properties of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e5fcaf0-f160-4cff-9e9d-44766e0545c9">HashEquivalentIncremental</a>
</td>
<td align="left" width="63%">
Incrementally generates a hash code for a subset of the tuning properties of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41495662-835b-47bc-a8d6-b0b689ec4d51">HashExact</a>
</td>
<td align="left" width="63%">
Generates a hash code for all of the tuning properties of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ddf2545-83a6-4b5d-94ba-7034aed61f08">HashExactIncremental</a>
</td>
<td align="left" width="63%">
Incrementally generates a hash code for all of the tuning properties of an object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDAComparable)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

