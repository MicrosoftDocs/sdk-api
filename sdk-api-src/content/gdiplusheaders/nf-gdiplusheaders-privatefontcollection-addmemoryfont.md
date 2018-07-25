---
UID: NF:gdiplusheaders.PrivateFontCollection.AddMemoryFont
title: PrivateFontCollection::AddMemoryFont
author: windows-sdk-content
description: The PrivateFontCollection::AddMemoryFont method adds a font that is contained in system memory to a Windows GDI+ font collection.
old-location: gdiplus\_gdiplus_CLASS_PrivateFontCollection_AddMemoryFont_memory_length_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\privatefontcollectionclass\privatefontcollectionmethods\addmemoryfont.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AddMemoryFont, AddMemoryFont method [GDI+], AddMemoryFont method [GDI+],PrivateFontCollection class, PrivateFontCollection class [GDI+],AddMemoryFont method, PrivateFontCollection.AddMemoryFont, PrivateFontCollection::AddMemoryFont, _gdiplus_CLASS_PrivateFontCollection_AddMemoryFont_memory_length_, gdiplus._gdiplus_CLASS_PrivateFontCollection_AddMemoryFont_memory_length_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources. 
The operating system requires elevated privileges to assure that all installed fonts are trusted. 





## -see-also




<a href="https://msdn.microsoft.com/ae12afcf-12cc-4c84-9aba-de56fc39437b">Creating a Private Font Collection</a>



<a href="https://msdn.microsoft.com/b53cc1cd-9dc8-4e93-9f92-7ebed7d034b6">PrivateFontCollection</a>



<a href="https://msdn.microsoft.com/f381b4eb-341a-437d-86dd-740c1d6108be">PrivateFontCollection::AddFontFile</a>



<a href="https://msdn.microsoft.com/12bc38c3-5fbc-4d7b-902c-92a5f5057473">Using Text and Fonts</a>
 

 

