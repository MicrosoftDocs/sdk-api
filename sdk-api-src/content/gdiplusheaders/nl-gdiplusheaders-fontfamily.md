---
UID: NL:gdiplusheaders.FontFamily
title: FontFamily (gdiplusheaders.h)
description: This FontFamily class encapsulates a set of fonts that make up a font family. A font family is a group of fonts that have the same typeface but different styles.
helpviewer_keywords: ["FontFamily","FontFamily class [GDI+]","FontFamily class [GDI+]","described","_gdiplus_CLASS_FontFamily_Class","gdiplus._gdiplus_CLASS_FontFamily_Class","gdiplusheaders/FontFamily"]
old-location: gdiplus\_gdiplus_CLASS_FontFamily_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamily.htm
ms.date: 12/05/2018
ms.keywords: FontFamily, FontFamily class [GDI+], FontFamily class [GDI+],described, _gdiplus_CLASS_FontFamily_Class, gdiplus._gdiplus_CLASS_FontFamily_Class, gdiplusheaders/FontFamily
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
 - FontFamily
 - gdiplusheaders/FontFamily
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
 - FontFamily
---

# FontFamily class


## -description

This <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-fontfamily(constfontfamily_)">FontFamily</a> class encapsulates a set of fonts that make up a font family. A font family is a group of fonts that have the same typeface but different styles.

## -remarks

Only regular, bold, italic, and bold italic are abstracted into the family, other styles, such as Narrow or Black, are considered separate font families. For example Times New Roman is a font family. The Times New Roman font family includes regular, bold, italic, and bold italic.