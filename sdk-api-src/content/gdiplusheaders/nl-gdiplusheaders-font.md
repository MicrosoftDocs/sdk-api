---
UID: NL:gdiplusheaders.Font
title: Font (gdiplusheaders.h)
description: The Font class encapsulates the characteristics, such as family, height, size, and style (or combination of styles), of a specific font. A Font object is used when drawing strings.
helpviewer_keywords: ["Font","Font class [GDI+]","Font class [GDI+]","described","_gdiplus_CLASS_Font_Class","gdiplus._gdiplus_CLASS_Font_Class","gdiplusheaders/Font"]
old-location: gdiplus\_gdiplus_CLASS_Font_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\font.htm
ms.date: 12/05/2018
ms.keywords: Font, Font class [GDI+], Font class [GDI+],described, _gdiplus_CLASS_Font_Class, gdiplus._gdiplus_CLASS_Font_Class, gdiplusheaders/Font
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
 - Font
 - gdiplusheaders/Font
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
 - Font
---

# Font class


## -description

The <b>Font</b> class encapsulates the characteristics, such as family, height, size, and style (or combination of styles), of a specific font. A <b>Font</b> object is used when drawing strings.

## -remarks

When using GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted.

