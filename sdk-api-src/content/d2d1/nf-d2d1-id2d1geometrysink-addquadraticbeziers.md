---
UID: NF:d2d1.ID2D1GeometrySink.AddQuadraticBeziers
title: ID2D1GeometrySink::AddQuadraticBeziers
author: windows-sdk-content
description: Adds a sequence of quadratic Bezier segments as an array in a single call.
old-location: direct2d\ID2D1GeometrySink_AddQuadraticBeziers.htm
tech.root: Direct2D
ms.assetid: 3eb0921e-1d9c-48a0-a709-3ac7feed22c5
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: AddQuadraticBeziers, AddQuadraticBeziers method [Direct2D], AddQuadraticBeziers method [Direct2D],ID2D1GeometrySink interface, ID2D1GeometrySink interface [Direct2D],AddQuadraticBeziers method, ID2D1GeometrySink.AddQuadraticBeziers, ID2D1GeometrySink::AddQuadraticBeziers, d2d1/ID2D1GeometrySink::AddQuadraticBeziers, direct2d.ID2D1GeometrySink_AddQuadraticBeziers
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1GeometrySink.AddQuadraticBeziers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GeometrySink::AddQuadraticBeziers


## -description


Adds a sequence of quadratic Bezier segments as an array in a single call.


## -parameters




### -param beziers [in]

Type: <b>const <a href="https://msdn.microsoft.com/5060cb17-b6f4-4796-b91d-602fd81591c2">D2D1_QUADRATIC_BEZIER_SEGMENT</a>*</b>

An array of a sequence of quadratic Bezier segments.


### -param beziersCount

TBD




#### - bezierCount

Type: <b>UINT</b>

A value indicating the number of quadratic Bezier segments in <i>beziers</i>. 


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>
 

 

