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

# PtVisible function


## -description


The <b>PtVisible</b> function determines whether the specified point is within the clipping region of a device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x

TBD


### -param y

TBD




#### - X [in]

The x-coordinate, in logical units, of the point.


#### - Y [in]

The y-coordinate, in logical units, of the point.


## -returns



If the specified point is within the clipping region of the device context, the return value is <b>TRUE</b>(1).

If the specified point is not within the clipping region of the device context, the return value is <b>FALSE</b>(0).

If the <b>HDC</b> is not valid, the return value is (BOOL)-1.




## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/990e9b22-0ce3-42b8-a87e-32fd2f2bc2fb">RectVisible</a>
 

 

