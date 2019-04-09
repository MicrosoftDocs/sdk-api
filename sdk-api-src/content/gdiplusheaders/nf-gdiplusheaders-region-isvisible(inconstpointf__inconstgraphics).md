---
UID: NF:gdiplusheaders.Region.IsVisible(IN const PointF &,IN const Graphics)
title: Region::IsVisible(IN const PointF &,IN const Graphics) (gdiplusheaders.h)
author: windows-sdk-content
description: The Region::IsVisible method determines whether a point is inside this region.
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_PointF_point_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_11pointfamppoint_graphicsg.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN const PointF &,IN const Graphics), Region.IsVisible(const PointF&,const Graphics*), Region::IsVisible, Region::IsVisible(IN const PointF &,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_PointF_point_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_PointF_point_Graphics_g_
ms.topic: method
req.header: gdiplusheaders.h
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
 - Region.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::IsVisible(IN const PointF &,IN const Graphics)


## -description


The <b>Region::IsVisible</b> method determines whether a point is inside this region.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a></b>

Reference to a point to test. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the point. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the point is inside this region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  A region contains its border.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

