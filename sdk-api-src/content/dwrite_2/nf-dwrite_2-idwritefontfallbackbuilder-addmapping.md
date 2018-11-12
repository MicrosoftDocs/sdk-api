---
UID: NF:dwrite_2.IDWriteFontFallbackBuilder.AddMapping
title: IDWriteFontFallbackBuilder::AddMapping
author: windows-sdk-content
description: Appends a single mapping to the list. Call this once for each additional mapping.
old-location: directwrite\idwritefontfallbackbuilder_addmapping.htm
tech.root: DirectWrite
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AddMapping, AddMapping method [Direct Write], AddMapping method [Direct Write],IDWriteFontFallbackBuilder interface, IDWriteFontFallbackBuilder interface [Direct Write],AddMapping method, IDWriteFontFallbackBuilder.AddMapping, IDWriteFontFallbackBuilder::AddMapping, directwrite.idwritefontfallbackbuilder_addmapping, dwrite_2/IDWriteFontFallbackBuilder::AddMapping
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteFontFallbackBuilder.AddMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFallbackBuilder::AddMapping


## -description


Appends a single mapping to the list. Call this once for each additional mapping.


## -parameters




### -param ranges

Type: <b><a href="https://msdn.microsoft.com/93DC235F-7E61-44CE-A949-8ABBD1D62CFF">DWRITE_UNICODE_RANGE</a>*</b>

Unicode ranges that apply to this mapping.


### -param rangesCount

Type: <b>UINT32</b>

Number of Unicode ranges.


### -param targetFamilyNames [in]

Type: <b>const WCHAR**</b>

List of target family name strings.


### -param targetFamilyNamesCount

Type: <b>UINT32</b>

Number of target family names.


### -param fontCollection [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a></b>

Optional explicit font collection for this mapping.


### -param localeName [in, optional]

Type: <b>const WCHAR*</b>

Locale of the context.


### -param baseFamilyName [in, optional]

Type: <b>const WCHAR*</b>

Base family name to match against, if applicable.


### -param scale

Type: <b>FLOAT</b>

Scale factor to multiply the result target font by.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/462AC12E-C856-4D8F-83AF-FAC3221425C2">IDWriteFontFallbackBuilder</a>
 

 

