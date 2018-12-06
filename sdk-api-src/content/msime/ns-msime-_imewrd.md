---
UID: NS:msime._IMEWRD
title: "_IMEWRD"
author: windows-sdk-content
description: Contains data about a word in the Word data of the Microsoft IME dictionary.
old-location: intl\imewrd.htm
tech.root: Intl
ms.assetid: BC0D039A-7EB4-4A8D-B063-479CF4294FF0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIMEWRD, IMEWRD, IMEWRD structure [Internationalization for Windows Applications], PIMEWRD, PIMEWRD structure pointer [Internationalization for Windows Applications], _IMEWRD, intl.imewrd, msime/IMEWRD, msime/PIMEWRD"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: msime.h
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
 - HeaderDef
api_location:
 - Msime.h
api_name:
 - IMEWRD
product: Windows
targetos: Windows
req.typenames: IMEWRD, *PIMEWRD
req.redist: 
---

# _IMEWRD structure


## -description


Contains data about a word in the Word data of the Microsoft IME dictionary.


## -struct-fields




### -field pwchReading

The reading string.


### -field pwchDisplay

The display string.


### -field ulPos

POS (Part of Speech), defined as JPOS_***.


### -field nPos1

Not used.


### -field nPos2

Not used.


### -field rgulAttrs

Reserved.


### -field cbComment

Size of the comment, in bytes, of <b>pvComment</b>.


### -field uct

Type of comment. This must be one of the values of the <a href="https://msdn.microsoft.com/B4969E4E-1918-4963-B9F2-606556FD5978">IMEUCT</a> enumeration.


### -field pvComment

Comment string.


## -see-also




<a href="https://msdn.microsoft.com/70BBC94A-97D6-4237-A0C9-F6861ED6C95D">IFEDictionary::ExistWord</a>



<a href="https://msdn.microsoft.com/9FEA7E1C-166B-4CA4-B25E-0406AD60AC0B">IFEDictionary::GetWords</a>



<a href="https://msdn.microsoft.com/551925ED-B05C-433F-91A9-D2BAC795E783">IFEDictionary::NextWords</a>



<a href="https://msdn.microsoft.com/CD79FBF5-E540-4B5C-A398-B7FE95F86701">IFEDictionary::RegisterWord</a>



<a href="https://msdn.microsoft.com/B4969E4E-1918-4963-B9F2-606556FD5978">IMEUCT</a>
 

 

