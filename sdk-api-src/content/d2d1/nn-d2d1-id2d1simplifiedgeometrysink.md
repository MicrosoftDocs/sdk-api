---
UID: NN:d2d1.ID2D1SimplifiedGeometrySink
title: ID2D1SimplifiedGeometrySink
author: windows-sdk-content
description: Describes a geometric path that does not contain quadratic bezier curves or arcs.
old-location: direct2d\ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: cf877a25-7b9f-4db0-ac53-b4a350795a86
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ID2D1SimplifiedGeometrySink, ID2D1SimplifiedGeometrySink interface [Direct2D], ID2D1SimplifiedGeometrySink interface [Direct2D],described, d2d1/ID2D1SimplifiedGeometrySink, direct2d.ID2D1SimplifiedGeometrySink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID2D1SimplifiedGeometrySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SimplifiedGeometrySink interface


## -description


Describes a geometric path that does not contain quadratic bezier curves or arcs. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SimplifiedGeometrySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1SimplifiedGeometrySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SimplifiedGeometrySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f079b38-b8ba-40b2-a5ed-4c9732cfd0c6">AddBeziers</a>
</td>
<td align="left" width="63%">
Creates a sequence of cubic Bezier curves and adds them to the geometry sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f9c5106-6a4e-4623-8ce5-6f21f0380976">AddLines</a>
</td>
<td align="left" width="63%">
Creates a sequence of lines using the specified points and adds them to the geometry sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a>
</td>
<td align="left" width="63%">
Starts a new figure at the specified point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dbbe5c6-d21c-4408-9208-53c7c051b22a">Close</a>
</td>
<td align="left" width="63%">
Closes the geometry sink, indicates whether it is in an error state, and resets the sink's error state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31f6aeba-2e81-4b8d-b734-0c501eae331f">EndFigure</a>
</td>
<td align="left" width="63%">
Ends the current figure; optionally, closes it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f60f48bb-989e-46a5-b77f-65da0b91a599">SetFillMode</a>
</td>
<td align="left" width="63%">
Specifies the method used to determine which points are inside the geometry described by this geometry sink  and which points are outside. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1162564-a39b-4c16-887e-ec06dd37301c">SetSegmentFlags</a>
</td>
<td align="left" width="63%">
Specifies stroke and join options to be applied to new segments added to the geometry sink.

</td>
</tr>
</table> 


## -remarks



A geometry sink consists of one or more figures. Each figure is made up of one or more line or Bezier curve segments. To create a figure, call the <a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">BeginFigure</a> method and specify the figure's start point, then use <a href="https://msdn.microsoft.com/3f9c5106-6a4e-4623-8ce5-6f21f0380976">AddLines</a> and <a href="https://msdn.microsoft.com/9f079b38-b8ba-40b2-a5ed-4c9732cfd0c6">AddBeziers</a> to add line and Bezier segments. When you are finished adding segments, call the <a href="https://msdn.microsoft.com/31f6aeba-2e81-4b8d-b734-0c501eae331f">EndFigure</a> method. You can repeat this sequence to create additional figures. When you are finished creating figures, call the <a href="https://msdn.microsoft.com/9dbbe5c6-d21c-4408-9208-53c7c051b22a">Close</a> method.

To create geometry paths that can contain arcs and quadratic Bezier curves, use an <a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

