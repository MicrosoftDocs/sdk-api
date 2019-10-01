---
UID: NL:gdiplusheaders.InstalledFontCollection
title: InstalledFontCollection (gdiplusheaders.h)
author: windows-sdk-content
description: The InstalledFontCollection class defines a class that represents the fonts installed on the system.
old-location: gdiplus\_gdiplus_CLASS_InstalledFontCollection_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\installedfontcollection.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InstalledFontCollection, InstalledFontCollection class [GDI+], InstalledFontCollection class [GDI+],described, _gdiplus_CLASS_InstalledFontCollection_Class, gdiplus._gdiplus_CLASS_InstalledFontCollection_Class, gdiplusheaders/InstalledFontCollection
ms.topic: class
f1_keywords: 
 - "gdiplusheaders/InstalledFontCollection"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - InstalledFontCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InstalledFontCollection class


## -description


The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-installedfontcollection-installedfontcollection(constinstalledfontcollection_)">InstalledFontCollection</a> class defines a class that represents the fonts installed on the system.


## -remarks



Windows GDI+ clients should not use the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-installedfontcollection-installedfontcollection(constinstalledfontcollection_)">InstalledFontCollection</a> class to install a font to Windows. Instead, use the Windows Graphics Device Interface (GDI)Â <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-addfontresourcea">AddFontResource</a> function. An <b>InstalledFontCollection</b> object can find only those fonts that were installed in Windows before the object was created.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontcollection">FontCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
 

 

