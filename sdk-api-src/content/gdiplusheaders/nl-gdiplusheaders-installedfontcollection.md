---
UID: NL:gdiplusheaders.InstalledFontCollection
title: InstalledFontCollection
author: windows-sdk-content
description: The InstalledFontCollection class defines a class that represents the fonts installed on the system.
old-location: gdiplus\_gdiplus_CLASS_InstalledFontCollection_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\installedfontcollection.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InstalledFontCollection, InstalledFontCollection class [GDI+], InstalledFontCollection class [GDI+],described, _gdiplus_CLASS_InstalledFontCollection_Class, gdiplus._gdiplus_CLASS_InstalledFontCollection_Class, gdiplusheaders/InstalledFontCollection
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InstalledFontCollection class


## -description


The <a href="https://msdn.microsoft.com/en-us/library/ms535364(v=VS.85).aspx">InstalledFontCollection</a> class defines a class that represents the fonts installed on the system.


## -remarks



Windows GDI+ clients should not use the <a href="https://msdn.microsoft.com/en-us/library/ms535364(v=VS.85).aspx">InstalledFontCollection</a> class to install a font to Windows. Instead, use the Windows Graphics Device Interface (GDI)Â <a href="https://msdn.microsoft.com/e553a25a-f281-4ddc-8e95-1f61ed8238f9">AddFontResource</a> function. An <b>InstalledFontCollection</b> object can find only those fonts that were installed in Windows before the object was created.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534438(v=VS.85).aspx">FontCollection</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533817(v=VS.85).aspx">Using Text and Fonts</a>
 

 

