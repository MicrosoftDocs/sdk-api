---
UID: NF:gdiplusheaders.Region.Union(IN const GraphicsPath)
title: Region::Union(IN const GraphicsPath) (gdiplusheaders.h)
description: The Region::Union method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified path's interior.
old-location: gdiplus\_gdiplus_CLASS_Region_Union_path_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionunionmethods\union_83path.htm
ms.date: 12/05/2018
ms.keywords: Region class [GDI+],Union method, Region.Union, Region.Union(IN const GraphicsPath), Region.Union(const GraphicsPath*), Region::Union, Region::Union(IN const GraphicsPath), Union, Union method [GDI+], Union method [GDI+],Region class, _gdiplus_CLASS_Region_Union_path_, gdiplus._gdiplus_CLASS_Region_Union_path_
f1_keywords:
- gdiplusheaders/Region.Union
dev_langs:
- c++
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
- Region.Union
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Region::Union(IN const GraphicsPath)


## -description


The <b>Region::Union</b> method updates this region to all portions (intersecting and nonintersecting) of itself and all portions of the specified path's interior.


## -parameters




### -param path [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object that specifies the path to use to update this 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

