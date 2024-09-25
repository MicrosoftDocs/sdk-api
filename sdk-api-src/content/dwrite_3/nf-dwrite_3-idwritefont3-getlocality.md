---
UID: NF:dwrite_3.IDWriteFont3.GetLocality
title: IDWriteFont3::GetLocality (dwrite_3.h)
description: Gets the current locality of the font.
helpviewer_keywords: ["GetLocality","GetLocality method [Direct Write]","GetLocality method [Direct Write]","IDWriteFont3 interface","IDWriteFont3 interface [Direct Write]","GetLocality method","IDWriteFont3.GetLocality","IDWriteFont3::GetLocality","directwrite.idwritefont3_getlocality","dwrite_3/IDWriteFont3::GetLocality"]
old-location: directwrite\idwritefont3_getlocality.htm
tech.root: DirectWrite
ms.assetid: B7CD16AE-77A3-4C3C-91B7-3AD32DCF68C0
ms.date: 12/05/2018
ms.keywords: GetLocality, GetLocality method [Direct Write], GetLocality method [Direct Write],IDWriteFont3 interface, IDWriteFont3 interface [Direct Write],GetLocality method, IDWriteFont3.GetLocality, IDWriteFont3::GetLocality, directwrite.idwritefont3_getlocality, dwrite_3/IDWriteFont3::GetLocality
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFont3::GetLocality
 - dwrite_3/IDWriteFont3::GetLocality
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFont3.GetLocality
---

# IDWriteFont3::GetLocality


## -description

Gets the current locality of the font.



## -returns

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality">DWRITE_LOCALITY</a></b>

Returns the current locality of the font.

## -remarks

For fully local files, the result will always  be DWRITE_LOCALITY_LOCAL. A downloadable file may be any of the states, and this function may change between calls.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a>

