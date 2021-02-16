---
UID: NF:gdiplusheaders.Region.Xor(constGraphicsPath)
title: Region::Xor(IN const GraphicsPath) (gdiplusheaders.h)
description: The Region::Xor method updates this region to the nonintersecting portions of itself and the specified path's interior.
helpviewer_keywords: ["Region class [GDI+]","Xor method","Region.Xor","Region.Xor(IN const GraphicsPath)","Region.Xor(const GraphicsPath*)","Region::Xor","Region::Xor(IN const GraphicsPath)","Xor","Xor method [GDI+]","Xor method [GDI+]","Region class","_gdiplus_CLASS_Region_Xor_path_","gdiplus._gdiplus_CLASS_Region_Xor_path_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Xor_path_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionxormethods\xor.htm
ms.date: 12/05/2018
ms.keywords: Region class [GDI+],Xor method, Region.Xor, Region.Xor(IN const GraphicsPath), Region.Xor(const GraphicsPath*), Region::Xor, Region::Xor(IN const GraphicsPath), Xor, Xor method [GDI+], Xor method [GDI+],Region class, _gdiplus_CLASS_Region_Xor_path_, gdiplus._gdiplus_CLASS_Region_Xor_path_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Region::Xor
 - gdiplusheaders/Region::Xor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.Xor
---

# Region::Xor(IN const GraphicsPath)


## -description

The <b>Region::Xor</b> method updates this region to the nonintersecting portions of itself and the specified path's interior.

## -parameters

### -param path [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> that specifies the path to use to update this region.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>