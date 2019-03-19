---
UID: NF:dwrite_3.IDWriteStringList.GetLocaleNameLength
title: IDWriteStringList::GetLocaleNameLength (dwrite_3.h)
author: windows-sdk-content
description: Gets the length in characters (not including the null terminator) of the locale name with the specified index.
old-location: directwrite\idwritestringlist_getlocalenamelength.htm
tech.root: DirectWrite
ms.assetid: AB3CDFB6-8B3E-47B1-BB19-C22E0D8D2D5C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLocaleNameLength, GetLocaleNameLength method [Direct Write], GetLocaleNameLength method [Direct Write],IDWriteStringList interface, IDWriteStringList interface [Direct Write],GetLocaleNameLength method, IDWriteStringList.GetLocaleNameLength, IDWriteStringList::GetLocaleNameLength, directwrite.idwritestringlist_getlocalenamelength, dwrite_3/IDWriteStringList::GetLocaleNameLength
ms.topic: method
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteStringList.GetLocaleNameLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteStringList::GetLocaleNameLength


## -description


Gets the length in characters (not including the null terminator) of the locale name with the specified index.


## -parameters




### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the locale name.


### -param length [out]

Type: <b>UINT32*</b>

Receives the length in characters, not including the null terminator.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07A61B37-C63D-4F7D-888C-96B56F30F477">IDWriteStringList</a>
 

 

