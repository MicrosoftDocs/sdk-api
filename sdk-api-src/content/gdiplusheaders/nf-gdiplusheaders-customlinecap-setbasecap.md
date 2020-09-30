---
UID: NF:gdiplusheaders.CustomLineCap.SetBaseCap
title: CustomLineCap::SetBaseCap (gdiplusheaders.h)
description: The CustomLineCap::SetBaseCap method sets the LineCap that appears as part of this CustomLineCap at the end of a line.
helpviewer_keywords: ["CustomLineCap class [GDI+]","SetBaseCap method","CustomLineCap.SetBaseCap","CustomLineCap::SetBaseCap","SetBaseCap","SetBaseCap method [GDI+]","SetBaseCap method [GDI+]","CustomLineCap class","_gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_","gdiplus._gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setbasecap.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],SetBaseCap method, CustomLineCap.SetBaseCap, CustomLineCap::SetBaseCap, SetBaseCap, SetBaseCap method [GDI+], SetBaseCap method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_, gdiplus._gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_
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
 - CustomLineCap::SetBaseCap
 - gdiplusheaders/CustomLineCap::SetBaseCap
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
 - CustomLineCap.SetBaseCap
---

# CustomLineCap::SetBaseCap


## -description

The <b>CustomLineCap::SetBaseCap</b> method sets the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> that appears as part of this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a> at the end of a line.

## -parameters

### -param baseCap [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that specifies the line cap used on the ends of the line to be drawn.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>