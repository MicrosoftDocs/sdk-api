---
UID: NF:gdiplusheaders.PrivateFontCollection.AddMemoryFont
title: PrivateFontCollection::AddMemoryFont (gdiplusheaders.h)
author: windows-sdk-content
description: The PrivateFontCollection::AddMemoryFont method adds a font that is contained in system memory to a Windows GDI+ font collection.
old-location: gdiplus\_gdiplus_CLASS_PrivateFontCollection_AddMemoryFont_memory_length_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\privatefontcollectionclass\privatefontcollectionmethods\addmemoryfont.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddMemoryFont, AddMemoryFont method [GDI+], AddMemoryFont method [GDI+],PrivateFontCollection class, PrivateFontCollection class [GDI+],AddMemoryFont method, PrivateFontCollection.AddMemoryFont, PrivateFontCollection::AddMemoryFont, _gdiplus_CLASS_PrivateFontCollection_AddMemoryFont_memory_length_, gdiplus._gdiplus_CLASS_PrivateFontCollection_AddMemoryFont_memory_length_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PrivateFontCollection.AddMemoryFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# PrivateFontCollection::AddMemoryFont


## -description


The <b>PrivateFontCollection::AddMemoryFont</b> method adds a font that is contained in system memory to a Windows GDI+ font collection. 


## -parameters




### -param memory [in]

Type: <b>const VOID*</b>

Pointer to a font that is contained in memory. 


### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of bytes of data in the font. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted. 





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-a-private-font-collection-use">Creating a Private Font Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection">PrivateFontCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile">PrivateFontCollection::AddFontFile</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
 

 

