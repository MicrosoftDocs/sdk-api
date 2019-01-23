---
UID: NF:dwrite_3.IDWriteStringList.GetStringLength
title: IDWriteStringList::GetStringLength
author: windows-sdk-content
description: Gets the length in characters (not including the null terminator) of the string with the specified index.
old-location: directwrite\idwritestringlist_getstringlength.htm
tech.root: DirectWrite
ms.assetid: 5511DD28-22B1-4006-A724-13C2C4A17E6C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStringLength, GetStringLength method [Direct Write], GetStringLength method [Direct Write],IDWriteStringList interface, IDWriteStringList interface [Direct Write],GetStringLength method, IDWriteStringList.GetStringLength, IDWriteStringList::GetStringLength, directwrite.idwritestringlist_getstringlength, dwrite_3/IDWriteStringList::GetStringLength
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
 - IDWriteStringList.GetStringLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteStringList::GetStringLength


## -description


Gets the length in characters (not including the null terminator) of the string with the specified index.


## -parameters




### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the string.


### -param length [out]

Type: <b>UINT32*</b>

Receives the length in characters of the string, not including the null terminator.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07A61B37-C63D-4F7D-888C-96B56F30F477">IDWriteStringList</a>
 

 

