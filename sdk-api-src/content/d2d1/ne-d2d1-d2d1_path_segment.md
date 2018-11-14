---
UID: NE:d2d1.D2D1_PATH_SEGMENT
title: D2D1_PATH_SEGMENT
author: windows-sdk-content
description: Indicates whether a segment should be stroked and whether the join between this segment and the previous one should be smooth. This enumeration allows a bitwise combination of its member values.
old-location: direct2d\D2D1_PATH_SEGMENT.htm
tech.root: direct2d
ms.assetid: 375a0a40-ec98-4f41-9c15-d284f8b17a73
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D2D1_PATH_SEGMENT, D2D1_PATH_SEGMENT enumeration [Direct2D], D2D1_PATH_SEGMENT_FORCE_ROUND_LINE_JOIN, D2D1_PATH_SEGMENT_FORCE_UNSTROKED, D2D1_PATH_SEGMENT_NONE, d2d1/D2D1_PATH_SEGMENT, d2d1/D2D1_PATH_SEGMENT_FORCE_ROUND_LINE_JOIN, d2d1/D2D1_PATH_SEGMENT_FORCE_UNSTROKED, d2d1/D2D1_PATH_SEGMENT_NONE, direct2d.D2D1_PATH_SEGMENT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_PATH_SEGMENT
product: Windows
targetos: Windows
req.typenames: D2D1_PATH_SEGMENT
req.redist: 
---

# D2D1_PATH_SEGMENT enumeration


## -description


Indicates whether a segment should be stroked and whether the join between this segment and the previous one should be smooth. This enumeration allows a bitwise combination of its member values. 


## -enum-fields




### -field D2D1_PATH_SEGMENT_NONE

The segment is joined  as specified by the <a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a> interface, and it is stroked. 


### -field D2D1_PATH_SEGMENT_FORCE_UNSTROKED

The segment is not stroked.


### -field D2D1_PATH_SEGMENT_FORCE_ROUND_LINE_JOIN

The segment is always joined with the one preceding it using a round line join, regardless of which <a href="https://msdn.microsoft.com/en-us/library/Dd368130(v=VS.85).aspx">D2D1_LINE_JOIN</a>enumeration is specified by the <a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a> interface. If this segment is the first segment and the figure is closed, a round line join is used to connect the closing segment with the first segment. If the figure is not closed, this setting has no effect on the first segment of the figure. If <a href="https://msdn.microsoft.com/e1162564-a39b-4c16-887e-ec06dd37301c">ID2D1SimplifiedGeometrySink::SetSegmentFlags</a> is called just before <a href="https://msdn.microsoft.com/31f6aeba-2e81-4b8d-b734-0c501eae331f">ID2D1SimplifiedGeometrySink::EndFigure</a>, the join between the closing segment and the last explicitly specified segment is affected.


### -field D2D1_PATH_SEGMENT_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/e1162564-a39b-4c16-887e-ec06dd37301c">ID2D1SimplifiedGeometrySink::SetSegmentFlags</a>



<a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>
 

 

