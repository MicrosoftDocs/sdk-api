---
UID: NL:gdipluslinecaps.AdjustableArrowCap
title: AdjustableArrowCap (gdipluslinecaps.h)
description: The AdjustableArrowCap class is a subclass of the CustomLineCap. This class builds a line cap that looks like an arrow.
helpviewer_keywords: ["AdjustableArrowCap","AdjustableArrowCap class [GDI+]","AdjustableArrowCap class [GDI+]","described","_gdiplus_CLASS_AdjustableArrowCap_Class","gdiplus._gdiplus_CLASS_AdjustableArrowCap_Class","gdipluslinecaps/AdjustableArrowCap"]
old-location: gdiplus\_gdiplus_CLASS_AdjustableArrowCap_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\adjustablearrowcap.htm
ms.date: 12/05/2018
ms.keywords: AdjustableArrowCap, AdjustableArrowCap class [GDI+], AdjustableArrowCap class [GDI+],described, _gdiplus_CLASS_AdjustableArrowCap_Class, gdiplus._gdiplus_CLASS_AdjustableArrowCap_Class, gdipluslinecaps/AdjustableArrowCap
req.header: gdipluslinecaps.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AdjustableArrowCap
 - gdipluslinecaps/AdjustableArrowCap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluslinecaps.h
api_name:
 - AdjustableArrowCap
---

# AdjustableArrowCap class


## -description

The <b>AdjustableArrowCap</b> class is a subclass of the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>. This class builds a line cap that looks like an arrow.

## -remarks

A line cap is the shape on the end of a line. Use the 
				<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomstartcap">Pen::SetCustomStartCap</a> and 
				<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomendcap">Pen::SetCustomEndCap</a> methods to associate an <b>AdjustableArrowCap</b> object with a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.