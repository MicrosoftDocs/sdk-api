---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.AddLines
title: ID2D1SimplifiedGeometrySink::AddLines
author: windows-sdk-content
description: Creates a sequence of lines using the specified points and adds them to the geometry sink.
old-location: direct2d\ID2D1SimplifiedGeometrySink_AddLines.htm
tech.root: direct2d
ms.assetid: 3f9c5106-6a4e-4623-8ce5-6f21f0380976
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: AddLines, AddLines method [Direct2D], AddLines method [Direct2D],ID2D1SimplifiedGeometrySink interface, ID2D1SimplifiedGeometrySink interface [Direct2D],AddLines method, ID2D1SimplifiedGeometrySink.AddLines, ID2D1SimplifiedGeometrySink::AddLines, d2d1/ID2D1SimplifiedGeometrySink::AddLines, direct2d.ID2D1SimplifiedGeometrySink_AddLines
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
 - ID2D1SimplifiedGeometrySink.AddLines
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SimplifiedGeometrySink::AddLines


## -description


Creates a sequence of lines using the specified points and adds them to the geometry sink.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

A pointer to an array of one or more points that describe the lines to draw. A line is drawn from the geometry sink's current point (the end point of the last segment drawn or the location specified by <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>) to the first point in the array. if the array contains additional points, a line is drawn from the first point to the second point in the array, from the second point to the third point, and so on.   


### -param pointsCount

Type: <b>UINT</b>

The number of points in the <i>points</i> array.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>
 

 

