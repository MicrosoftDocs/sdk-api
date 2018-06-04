---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# AdjustableArrowCap::AdjustableArrowCap(IN REAL,IN REAL,IN BOOL)


## -description


Creates an adjustable arrow line cap with the specified height and width. The arrow line cap can be filled or nonfilled. The middle inset defaults to zero.


## -parameters




#### - height [in]

Type: <b>REAL</b>

Real number that specifies the length, in units, of the arrow from its base to its point. 


#### - width [in]

Type: <b>REAL</b>

Real number that specifies the distance, in units, between the corners of the base of the arrow. 


#### - isFilled [in]

Type: <b>BOOL</b>

Boolean value that specifies whether the arrow is filled. The default value is <b>TRUE</b>. 


## -remarks



The middle inset is the number of units that the midpoint of the base shifts towards the vertex. A middle inset of zero results in no shift — the base is a straight line, giving the arrow a triangular shape. A positive (greater than zero) middle inset results in a shift the specified number of units toward the vertex — the base is an arrow shape that points toward the vertex, giving the arrow cap a V-shape. A negative (less than zero) middle inset results in a shift the specified number of units away from the vertex — the base becomes an arrow shape that points away from the vertex, giving the arrow either a diamond shape (if the absolute value of the middle inset is equal to the height) or distorted diamond shape. If the middle inset is equal to or greater than the height of the arrow cap, the cap does not appear at all. The value of the middle inset affects the arrow cap only if the arrow cap is filled. The middle inset defaults to zero when an <b>AdjustableArrowCap::AdjustableArrowCap</b> object is constructed.




## -see-also




<a href="https://msdn.microsoft.com/da4a0644-eedf-4a9c-935a-e9fa822b2673">AdjustableArrowCap</a>



<a href="https://msdn.microsoft.com/83bc6530-9d78-49ad-9dfc-ea9776945ae6">AdjustableArrowCap::GetMiddleInset</a>



<a href="https://msdn.microsoft.com/67721251-b805-425f-9742-6afed25df831">AdjustableArrowCap::SetMiddleInset</a>
 

 

