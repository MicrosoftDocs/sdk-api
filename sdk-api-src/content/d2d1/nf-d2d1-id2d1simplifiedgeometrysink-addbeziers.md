---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.AddBeziers
title: ID2D1SimplifiedGeometrySink::AddBeziers
author: windows-sdk-content
description: Creates a sequence of cubic Bezier curves and adds them to the geometry sink.
old-location: direct2d\ID2D1SimplifiedGeometrySink_AddBeziers.htm
tech.root: direct2d
ms.assetid: 9f079b38-b8ba-40b2-a5ed-4c9732cfd0c6
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AddBeziers, AddBeziers method [Direct2D], AddBeziers method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],AddBeziers method, ID2D1SimplifiedGeometrySink.AddBeziers, ID2D1SimplifiedGeometrySink::AddBeziers, d2d1/ID2D1SimplifiedGeometrySink::AddBeziers, direct2d.ID2D1SimplifiedGeometrySink_AddBeziers
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
 - ID2D1SimplifiedGeometrySink.AddBeziers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1SimplifiedGeometrySink.AddBeziers
: 
---

# ID2D1SimplifiedGeometrySink::AddBeziers


## -description


Creates a sequence of cubic Bezier curves and adds them to the geometry sink.


## -parameters




### -param beziers [in]

Type: <b>const <a href="https://msdn.microsoft.com/cf8df7d2-c4fe-4a46-a4b2-7e0eed67df2a">D2D1_BEZIER_SEGMENT</a>*</b>

A pointer to an array of Bezier segments that describes the Bezier curves to create. A curve is drawn from the geometry sink's current point (the end point of the last segment drawn or the location specified by <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>) to the end point of the first Bezier segment in the array. if the array contains additional Bezier segments, each subsequent Bezier segment uses the end point of the preceding Bezier segment as its start point.


### -param beziersCount

Type: <b>UINT</b>

The number of Bezier segments in the <i>beziers</i> array.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>
 

 

