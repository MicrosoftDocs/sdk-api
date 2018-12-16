---
UID: NF:dwrite.IDWriteFontCollection.FindFamilyName
title: IDWriteFontCollection::FindFamilyName
author: windows-sdk-content
description: Finds the font family with the specified family name.
old-location: directwrite\IDWriteFontCollection_FindFamilyName.htm
tech.root: DirectWrite
ms.assetid: 5537988f-aba0-4477-be01-72a5f8e66395
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindFamilyName, FindFamilyName method [Direct Write], FindFamilyName method [Direct Write],IDWriteFontCollection interface, IDWriteFontCollection interface [Direct Write],FindFamilyName method, IDWriteFontCollection.FindFamilyName, IDWriteFontCollection::FindFamilyName, directwrite.IDWriteFontCollection_FindFamilyName, dwrite/IDWriteFontCollection::FindFamilyName
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFontCollection.FindFamilyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontCollection::FindFamilyName


## -description


 Finds the font family with the specified family name.


## -parameters




### -param familyName [in]

Type: <b>const WCHAR*</b>

An array of characters, which is null-terminated, containing the name of the font family. The name is not case-sensitive but must otherwise exactly match a family name in the collection.


### -param index [out]

Type: <b>UINT32*</b>

When this method returns, contains the zero-based index of the matching font family if the family name was found; otherwise, <b>UINT_MAX</b>.


### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, <b>TRUE</b> if the family name exists; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>
 

 

