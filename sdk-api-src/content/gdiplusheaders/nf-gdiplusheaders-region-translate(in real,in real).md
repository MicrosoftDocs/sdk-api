---
UID: NF:gdiplusheaders.Region.Translate(IN REAL,IN REAL)
title: Region::Translate(IN REAL,IN REAL)
author: windows-sdk-content
description: The Region::Translate method offsets this region by specified amounts in the horizontal and vertical directions.
old-location: gdiplus\_gdiplus_CLASS_Region_Translate_REAL_dx_REAL_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regiontranslatemethods\translate_17realdx_realdy.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Region class [GDI+],Translate method, Region.Translate, Region.Translate(IN REAL,IN REAL), Region.Translate(REAL,REAL), Region::Translate, Region::Translate(IN REAL,IN REAL), Translate, Translate method [GDI+], Translate method [GDI+],Region class, _gdiplus_CLASS_Region_Translate_REAL_dx_REAL_dy_, gdiplus._gdiplus_CLASS_Region_Translate_REAL_dx_REAL_dy_
ms.prod: windows-hardware
ms.technology: windows-devices
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

# Region::Translate(IN REAL,IN REAL)


## -description


The <b>Region::Translate</b> method offsets this region by specified amounts in the horizontal and vertical directions.


## -parameters




### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the amount to shift the region in the x direction. 


### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the amount to shift the region in the y direction. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/7167032f-7cb2-4565-bc5b-c04b416936fd">Region::Transform</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

