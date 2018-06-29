---
UID: NL:gdiplusheaders.PrivateFontCollection
title: PrivateFontCollection
author: windows-sdk-content
description: The PrivateFontCollection is a collection class for fonts. This class keeps a collection of fonts specifically for an application. The fonts in the collection can include installed fonts as well as fonts that have not been installed on the system.
old-location: gdiplus\_gdiplus_CLASS_PrivateFontCollection_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\privatefontcollection.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PrivateFontCollection, PrivateFontCollection class [GDI+], PrivateFontCollection class [GDI+],described, _gdiplus_CLASS_PrivateFontCollection_Class, gdiplus._gdiplus_CLASS_PrivateFontCollection_Class, gdiplusheaders/PrivateFontCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - PrivateFontCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# PrivateFontCollection class


## -description


The <b>PrivateFontCollection</b> is a collection class for fonts. This class keeps a collection of fonts specifically for an application. The fonts in the collection can include installed fonts as well as fonts that have not been installed on the system.


## -remarks



<b>PrivateFontCollection</b> allows applications to install a private version of an existing font without the need to replace the system version of the font. For example, GDI+ can create a private version of the Arial font in addition to the Arial font that the system uses. <b>PrivateFontCollection</b> can also be used to install fonts that don't exist in the operating system. This is a temporary font install that doesn't affect the system-installed collection. To see the installed collection use the 
				<a href="https://msdn.microsoft.com/library/ms534469(v=VS.85).aspx">InstalledFontCollection</a> class.

<div class="alert"><b>Note</b>  When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted.</div>
<div> </div>


