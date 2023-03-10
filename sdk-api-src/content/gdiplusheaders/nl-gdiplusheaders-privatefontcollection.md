---
UID: NL:gdiplusheaders.PrivateFontCollection
title: PrivateFontCollection (gdiplusheaders.h)
description: The PrivateFontCollection is a collection class for fonts. This class keeps a collection of fonts specifically for an application. The fonts in the collection can include installed fonts as well as fonts that have not been installed on the system.
helpviewer_keywords: ["PrivateFontCollection","PrivateFontCollection class [GDI+]","PrivateFontCollection class [GDI+]","described","_gdiplus_CLASS_PrivateFontCollection_Class","gdiplus._gdiplus_CLASS_PrivateFontCollection_Class","gdiplusheaders/PrivateFontCollection"]
old-location: gdiplus\_gdiplus_CLASS_PrivateFontCollection_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\privatefontcollection.htm
ms.date: 12/05/2018
ms.keywords: PrivateFontCollection, PrivateFontCollection class [GDI+], PrivateFontCollection class [GDI+],described, _gdiplus_CLASS_PrivateFontCollection_Class, gdiplus._gdiplus_CLASS_PrivateFontCollection_Class, gdiplusheaders/PrivateFontCollection
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
 - PrivateFontCollection
 - gdiplusheaders/PrivateFontCollection
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
 - PrivateFontCollection
---

# PrivateFontCollection class


## -description

The <b>PrivateFontCollection</b> is a collection class for fonts. This class keeps a collection of fonts specifically for an application. The fonts in the collection can include installed fonts as well as fonts that have not been installed on the system.

## -remarks

<b>PrivateFontCollection</b> allows applications to install a private version of an existing font without the need to replace the system version of the font. For example, GDI+ can create a private version of the Arial font in addition to the Arial font that the system uses. <b>PrivateFontCollection</b> can also be used to install fonts that don't exist in the operating system. This is a temporary font install that doesn't affect the system-installed collection. To see the installed collection use the 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection">InstalledFontCollection</a> class.

<div class="alert"><b>Note</b>  When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted.</div>
<div> </div>