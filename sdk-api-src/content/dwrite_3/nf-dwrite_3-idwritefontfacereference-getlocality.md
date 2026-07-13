---
UID: NF:dwrite_3.IDWriteFontFaceReference.GetLocality
title: IDWriteFontFaceReference::GetLocality (dwrite_3.h)
description: Get the locality of this font face reference.
helpviewer_keywords: ["GetLocality","GetLocality method [Direct Write]","GetLocality method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","GetLocality method","IDWriteFontFaceReference.GetLocality","IDWriteFontFaceReference::GetLocality","directwrite.idwritefontfacereference_getlocality","dwrite_3/IDWriteFontFaceReference::GetLocality"]
old-location: directwrite\idwritefontfacereference_getlocality.htm
tech.root: DirectWrite
ms.assetid: 533f30a7-bf54-670e-63be-ffb9b07fb9d8
ms.date: 09/10/2025
ms.keywords: GetLocality, GetLocality method [Direct Write], GetLocality method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],GetLocality method, IDWriteFontFaceReference.GetLocality, IDWriteFontFaceReference::GetLocality, directwrite.idwritefontfacereference_getlocality, dwrite_3/IDWriteFontFaceReference::GetLocality
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFaceReference::GetLocality
 - dwrite_3/IDWriteFontFaceReference::GetLocality
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFaceReference.GetLocality
---

# IDWriteFontFaceReference::GetLocality


## -description

Get the locality of this font face reference.



## -returns

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality">DWRITE_LOCALITY</a></b>

Returns the locality of this font face reference.

## -remarks

You can always successfully  
     create a font face from a fully local font. Attempting to create a font     
     face on a remote or partially local font may fail with DWRITE_E_REMOTEFONT.    
     This function may change between calls depending on background downloads    
     and whether cached data expires.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

