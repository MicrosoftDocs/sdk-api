---
UID: NF:d2d1.ID2D1LinearGradientBrush.GetGradientStopCollection
title: ID2D1LinearGradientBrush::GetGradientStopCollection (d2d1.h)
author: windows-sdk-content
description: Retrieves the ID2D1GradientStopCollection associated with this linear gradient brush.
old-location: direct2d\ID2D1LinearGradientBrush_GetGradientStopCollection.htm
tech.root: Direct2D
ms.assetid: 2433d8ed-112e-4620-b207-42bf9e084e23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGradientStopCollection, GetGradientStopCollection method [Direct2D], GetGradientStopCollection method [Direct2D],ID2D1LinearGradientBrush interface, ID2D1LinearGradientBrush interface [Direct2D],GetGradientStopCollection method, ID2D1LinearGradientBrush.GetGradientStopCollection, ID2D1LinearGradientBrush::GetGradientStopCollection, d2d1/ID2D1LinearGradientBrush::GetGradientStopCollection, direct2d.ID2D1LinearGradientBrush_GetGradientStopCollection
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
 - ID2D1LinearGradientBrush.GetGradientStopCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1LinearGradientBrush::GetGradientStopCollection


## -description


Retrieves the <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> associated with this linear gradient brush.


## -parameters




### -param gradientStopCollection [out]

Type: <b><a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>**</b>

The  <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> object associated with this linear gradient brush object. This parameter is passed uninitialized. 


## -returns



This method does not return a value.




## -remarks




<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> contains an array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures and information, such as the extend mode and the color interpolation mode.




## -see-also




<a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a>



<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>



<a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a>
 

 

