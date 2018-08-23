---
UID: NF:dwrite.IDWriteLocalizedStrings.GetLocaleNameLength
title: IDWriteLocalizedStrings::GetLocaleNameLength
author: windows-sdk-content
description: Gets the length in characters (not including the null terminator) of the locale name with the specified index.
old-location: directwrite\IDWriteLocalizedStrings_GetLocaleNameLength.htm
old-project: DirectWrite
ms.assetid: a175380b-1109-476d-8bd7-9ba0753c125f
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetLocaleNameLength, GetLocaleNameLength method [Direct Write], GetLocaleNameLength method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],GetLocaleNameLength method, IDWriteLocalizedStrings.GetLocaleNameLength, IDWriteLocalizedStrings::GetLocaleNameLength, directwrite.IDWriteLocalizedStrings_GetLocaleNameLength, dwrite/IDWriteLocalizedStrings::GetLocaleNameLength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteLocalizedStrings.GetLocaleNameLength
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteLocalizedStrings::GetLocaleNameLength


## -description


 Gets the length in characters (not including the null terminator) of the locale name with the specified index.


## -parameters




### -param index

Type: <b>UINT32</b>

Zero-based index of the locale name to be retrieved.


### -param length [out]

Type: <b>UINT32*</b>

When this method returns, contains the length in characters of the locale name, not including the null terminator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>
 

 

