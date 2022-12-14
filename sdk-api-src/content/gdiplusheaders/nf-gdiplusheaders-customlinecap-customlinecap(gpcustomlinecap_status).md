---
UID: NF:gdiplusheaders.CustomLineCap.CustomLineCap(GpCustomLineCap,Status)
title: CustomLineCap::CustomLineCap(GpCustomLineCap,Status) (gdiplusheaders.h)
description: Creates a CustomLineCap::CustomLineCap object. (overload 2/2)
helpviewer_keywords: ["CustomLineCap","CustomLineCap class [GDI+]","CustomLineCap constructor","CustomLineCap constructor [GDI+]","CustomLineCap constructor [GDI+]","CustomLineCap class","CustomLineCap.CustomLineCap","CustomLineCap.CustomLineCap(GpCustomLineCap","Status)","CustomLineCap::CustomLineCap","CustomLineCap::CustomLineCap(GpCustomLineCap","Status)","_gdiplus_CLASS_CustomLineCap_CustomLineCap_fillPath_strokePath_baseCap_baseInset_","gdiplus._gdiplus_CLASS_CustomLineCap_CustomLineCap_fillPath_strokePath_baseCap_baseInset_"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_CustomLineCap_fillPath_strokePath_baseCap_baseInset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecap_29fillpath_strokepath_basecap_baseinset.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap, CustomLineCap class [GDI+],CustomLineCap constructor, CustomLineCap constructor [GDI+], CustomLineCap constructor [GDI+],CustomLineCap class, CustomLineCap.CustomLineCap, CustomLineCap.CustomLineCap(GpCustomLineCap,Status), CustomLineCap::CustomLineCap, CustomLineCap::CustomLineCap(GpCustomLineCap,Status), _gdiplus_CLASS_CustomLineCap_CustomLineCap_fillPath_strokePath_baseCap_baseInset_, gdiplus._gdiplus_CLASS_CustomLineCap_CustomLineCap_fillPath_strokePath_baseCap_baseInset_
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
 - CustomLineCap::CustomLineCap
 - gdiplusheaders/CustomLineCap::CustomLineCap
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
 - CustomLineCap.CustomLineCap
---

## -description

Creates a <b>CustomLineCap::CustomLineCap</b> object.

## -parameters

### -param nativeCap

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a></b>

Optional. Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that specifies the line cap that will be used. The default value is LineCapFlat. 

### -param status

TBD

## -remarks

The 
				<i>fillPath</i> and 
				<i>strokePath</i> parameters cannot be used at the same time. You should pass <b>NULL</b> to one of those two parameters. If you pass nonnull values to both parameters, then 
				<i>fillPath</i> is ignored.

The <b>CustomLineCap::CustomLineCap</b> class uses the winding fill mode regardless of the fill mode that is set for the 
				<b>GraphicsPath</b> object passed to the <b>CustomLineCap::CustomLineCap</b> constructor.
