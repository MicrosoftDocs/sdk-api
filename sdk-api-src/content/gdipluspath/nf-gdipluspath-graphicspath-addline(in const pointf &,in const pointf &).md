---
UID: NF:gdipluspath.GraphicsPath.AddLine(IN const PointF &,IN const PointF &)
title: GraphicsPath::AddLine(IN const PointF &,IN const PointF &)
author: windows-sdk-content
description: The GraphicsPath::AddLine method adds a line to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddLine_PointF_pt1_PointF_pt2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddlinemethods\addline_30pointfamppt1_pointfamppt2.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddLine, AddLine method [GDI+], AddLine method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddLine method, GraphicsPath.AddLine, GraphicsPath.AddLine(IN const PointF &,IN const PointF &), GraphicsPath.AddLine(const PointF&,const PointF&), GraphicsPath::AddLine, GraphicsPath::AddLine(IN const PointF &,IN const PointF &), _gdiplus_CLASS_GraphicsPath_AddLine_PointF_pt1_PointF_pt2_, gdiplus._gdiplus_CLASS_GraphicsPath_AddLine_PointF_pt1_PointF_pt2_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.AddLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddLine(IN const PointF &,IN const PointF &)


## -description


The <b>GraphicsPath::AddLine</b> method adds a line to the current figure of this path.


## -parameters




### -param pt1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a></b>

Reference to a point at which to start the line. 


### -param pt2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a></b>

Reference to a point at which to end the line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/ff80b2a7-47a9-49dd-b2ea-9bd0453fac0b">AddLine Methods</a>



<a href="https://msdn.microsoft.com/39055c59-6d88-4b46-bc4c-cf2a4a927d29">AddLines Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

