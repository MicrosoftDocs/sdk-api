---
UID: NL:gdiplusheaders.CustomLineCap
title: CustomLineCap (gdiplusheaders.h)
description: The CustomLineCap class encapsulates a custom line cap.
helpviewer_keywords: ["CustomLineCap","CustomLineCap class [GDI+]","CustomLineCap class [GDI+]","described","_gdiplus_CLASS_CustomLineCap_Class","gdiplus._gdiplus_CLASS_CustomLineCap_Class","gdiplusheaders/CustomLineCap"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecap.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap, CustomLineCap class [GDI+], CustomLineCap class [GDI+],described, _gdiplus_CLASS_CustomLineCap_Class, gdiplus._gdiplus_CLASS_CustomLineCap_Class, gdiplusheaders/CustomLineCap
req.header: gdiplusheaders.h
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
 - CustomLineCap
 - gdiplusheaders/CustomLineCap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - CustomLineCap
---

# CustomLineCap class


## -description

The <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-customlinecap-customlinecap(constcustomlinecap_)">CustomLineCap</a> class encapsulates a custom line cap. A line cap defines the style of graphic used to draw the ends of a line. It can be various shapes, such as a square, circle, or diamond. A custom line cap is defined by the path that draws it. The path is drawn by using a 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to draw the outline of a shape or by using a 
			<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object to fill the interior. The cap can be used on either or both ends of the line. Spacing can be adjusted between the end caps and the line.