---
UID: NF:gdipluspath.GraphicsPath.IsVisible(IN REAL,IN REAL,IN const Graphics)
title: GraphicsPath::IsVisible(IN REAL,IN REAL,IN const Graphics) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::IsVisible method determines whether a specified point lies in the area that is filled when this path is filled by a specified Graphics object.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_IsVisible_REAL_x_REAL_y_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathisvisiblemethods\isvisible_68realx_realy_graphicsg.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GraphicsPath class [GDI+],IsVisible method, GraphicsPath.IsVisible, GraphicsPath.IsVisible(IN REAL,IN REAL,IN const Graphics), GraphicsPath.IsVisible(REAL,REAL,const Graphics*), GraphicsPath::IsVisible, GraphicsPath::IsVisible(IN REAL,IN REAL,IN const Graphics), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_IsVisible_REAL_x_REAL_y_Graphics_g_, gdiplus._gdiplus_CLASS_GraphicsPath_IsVisible_REAL_x_REAL_y_Graphics_g_
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
 - GraphicsPath.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::IsVisible(IN REAL,IN REAL,IN const Graphics)


## -description


The <b>GraphicsPath::IsVisible</b> method determines whether a specified point lies in the area that is filled when this path is filled by a specified <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters




### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the point to be tested. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the point to be tested. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that specifies a world-to-device transformation. If the value of this parameter is <b>NULL</b>, the test is done in world coordinates; otherwise, the test is done in device coordinates. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the test point lies in the interior of this path, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535562(v=VS.85).aspx">IsOutlineVisible Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535563(v=VS.85).aspx">IsVisible Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
 

 

