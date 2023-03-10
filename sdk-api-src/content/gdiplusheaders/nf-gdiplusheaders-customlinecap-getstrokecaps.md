---
UID: NF:gdiplusheaders.CustomLineCap.GetStrokeCaps
title: CustomLineCap::GetStrokeCaps (gdiplusheaders.h)
description: The CustomLineCap::GetStrokeCaps method gets the end cap styles for both the start line cap and the end line cap. Line caps are LineCap objects that end the individual lines within a path.
helpviewer_keywords: ["CustomLineCap class [GDI+]","GetStrokeCaps method","CustomLineCap.GetStrokeCaps","CustomLineCap::GetStrokeCaps","GetStrokeCaps","GetStrokeCaps method [GDI+]","GetStrokeCaps method [GDI+]","CustomLineCap class","_gdiplus_CLASS_CustomLineCap_GetStrokeCaps_startCap_endCap_","gdiplus._gdiplus_CLASS_CustomLineCap_GetStrokeCaps_startCap_endCap_"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_GetStrokeCaps_startCap_endCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\getstrokecaps.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],GetStrokeCaps method, CustomLineCap.GetStrokeCaps, CustomLineCap::GetStrokeCaps, GetStrokeCaps, GetStrokeCaps method [GDI+], GetStrokeCaps method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_GetStrokeCaps_startCap_endCap_, gdiplus._gdiplus_CLASS_CustomLineCap_GetStrokeCaps_startCap_endCap_
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
 - CustomLineCap::GetStrokeCaps
 - gdiplusheaders/CustomLineCap::GetStrokeCaps
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
 - CustomLineCap.GetStrokeCaps
---

# CustomLineCap::GetStrokeCaps


## -description

The <b>CustomLineCap::GetStrokeCaps</b> method gets the end cap styles for both the start line cap and the end line cap. Line caps are <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> objects that end the individual lines within a path.

## -parameters

### -param startCap [out]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>*</b>

Pointer to a variable that receives an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that indicates the line cap used at the start of the line to be drawn.

### -param endCap [out]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>*</b>

Pointer to a variable that receives an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that indicates the line cap used at the end of the line to be drawn.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>