---
UID: NF:d2d1.ID2D1GradientStopCollection.GetGradientStops
title: ID2D1GradientStopCollection::GetGradientStops
author: windows-sdk-content
description: Copies the gradient stops from the collection into an array of D2D1_GRADIENT_STOP structures.
old-location: direct2d\ID2D1GradientStopCollection_GetGradientStops.htm
tech.root: direct2d
ms.assetid: a5ae1b14-2694-4593-8eba-17d93b45bb9c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGradientStops, GetGradientStops method [Direct2D], GetGradientStops method [Direct2D],ID2D1GradientStopCollection interface, ID2D1GradientStopCollection interface [Direct2D],GetGradientStops method, ID2D1GradientStopCollection.GetGradientStops, ID2D1GradientStopCollection::GetGradientStops, d2d1/ID2D1GradientStopCollection::GetGradientStops, direct2d.ID2D1GradientStopCollection_GetGradientStops
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GradientStopCollection.GetGradientStops
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientStopCollection::GetGradientStops


## -description


Copies the gradient stops from the collection into an array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures.


## -parameters




### -param gradientStops [out]

Type: <b><a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>*</b>

A pointer to a one-dimensional array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures. When this method returns, the array contains copies of the collection's gradient stops. You must allocate the memory for this array.


### -param gradientStopsCount

Type: <b>UINT</b>

A value indicating the number of gradient stops to copy. If the value is less than the number of gradient stops in the collection, the remaining gradient stops are omitted. If the value is larger than the number of gradient stops in the collection, the extra gradient stops are set to <b>NULL</b>. To obtain the number of gradient stops in the collection, use the <a href="https://msdn.microsoft.com/1c3ef4b0-e781-4177-81a4-b39add8468a0">GetGradientStopCount</a> method.


## -returns



This method does not return a value.




## -remarks



Gradient stops are copied in order of position, starting with the gradient stop with the smallest position value and progressing to the gradient stop with the largest position value.




## -see-also




<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>
 

 

