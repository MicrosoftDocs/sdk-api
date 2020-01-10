---
UID: NF:dwrite_3.IDWriteFactory3.GetSystemFontSet
title: IDWriteFactory3::GetSystemFontSet (dwrite_3.h)
description: Retrieves the list of system fonts.
old-location: directwrite\idwritefactory3_getsystemfontset.htm
tech.root: DirectWrite
ms.assetid: 84fd8c9f-f4b1-3015-f431-08b7a07ff32b
ms.date: 12/05/2018
ms.keywords: GetSystemFontSet, GetSystemFontSet method [Direct Write], GetSystemFontSet method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],GetSystemFontSet method, IDWriteFactory3.GetSystemFontSet, IDWriteFactory3::GetSystemFontSet, directwrite.idwritefactory3_getsystemfontset, dwrite_3/IDWriteFactory3::GetSystemFontSet
f1_keywords:
- dwrite_3/IDWriteFactory3.GetSystemFontSet
dev_langs:
- c++
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- IDWriteFactory3.GetSystemFontSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory3::GetSystemFontSet


## -description


Retrieves the list of system fonts.


## -parameters




### -param fontSet [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>**</b>

Holds the newly created font set object, or NULL in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>
 

 

