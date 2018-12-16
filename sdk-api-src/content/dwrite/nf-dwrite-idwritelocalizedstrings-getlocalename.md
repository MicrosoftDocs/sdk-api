---
UID: NF:dwrite.IDWriteLocalizedStrings.GetLocaleName
title: IDWriteLocalizedStrings::GetLocaleName
author: windows-sdk-content
description: Copies the locale name with the specified index to the specified array.
old-location: directwrite\IDWriteLocalizedStrings_GetLocaleName.htm
tech.root: DirectWrite
ms.assetid: 9256845d-c75e-4def-8466-f3b796f74817
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLocaleName, GetLocaleName method [Direct Write], GetLocaleName method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],GetLocaleName method, IDWriteLocalizedStrings.GetLocaleName, IDWriteLocalizedStrings::GetLocaleName, directwrite.IDWriteLocalizedStrings_GetLocaleName, dwrite/IDWriteLocalizedStrings::GetLocaleName
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
 - IDWriteLocalizedStrings.GetLocaleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteLocalizedStrings::GetLocaleName


## -description


 Copies the locale name with the specified index to the specified array.


## -parameters




### -param index

Type: <b>UINT32</b>

Zero-based index of the locale name to be retrieved.


### -param localeName [out]

Type: <b>WCHAR*</b>

When this method returns, contains a character array, which is null-terminated, that receives the locale name from the language/string pair.  The buffer allocated for this array must be at least the size of <i>size</i>, in element count.


### -param size

Type: <b>UINT32</b>

The size of the array in characters. The size must include space for the terminating
     null character.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>
 

 

