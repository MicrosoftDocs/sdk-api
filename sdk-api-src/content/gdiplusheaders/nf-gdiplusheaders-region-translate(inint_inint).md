---
UID: NF:gdiplusheaders.Region.Translate(IN INT,IN INT)
title: Region::Translate(IN INT,IN INT) (gdiplusheaders.h)
author: windows-sdk-content
description: The Region::Translate method offsets this region by specified amounts in the horizontal and vertical directions.
old-location: gdiplus\_gdiplus_CLASS_Region_Translate_INT_dx_INT_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regiontranslatemethods\translate_28intdx_intdy.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Region class [GDI+],Translate method, Region.Translate, Region.Translate(IN INT,IN INT), Region.Translate(INT,INT), Region::Translate, Region::Translate(IN INT,IN INT), Translate, Translate method [GDI+], Translate method [GDI+],Region class, _gdiplus_CLASS_Region_Translate_INT_dx_INT_dy_, gdiplus._gdiplus_CLASS_Region_Translate_INT_dx_INT_dy_
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
 - Region.Translate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::Translate(IN INT,IN INT)


## -description


The <b>Region::Translate</b> method offsets this region by specified amounts in the horizontal and vertical directions.


## -parameters




### -param dx [in]

Type: <b>INT</b>

Integer that specifies the amount to shift the region in the x direction. 


### -param dy [in]

Type: <b>INT</b>

Integer that specifies the amount to shift the region in the y direction. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534784(v=VS.85).aspx">Region::Transform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

