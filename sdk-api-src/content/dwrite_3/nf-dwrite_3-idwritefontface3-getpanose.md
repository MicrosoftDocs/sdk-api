---
UID: NF:dwrite_3.IDWriteFontFace3.GetPanose
title: IDWriteFontFace3::GetPanose (dwrite_3.h)
description: Gets the PANOSE values from the font, used for font selection and matching.
helpviewer_keywords: ["GetPanose","GetPanose method [Direct Write]","GetPanose method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","GetPanose method","IDWriteFontFace3.GetPanose","IDWriteFontFace3::GetPanose","directwrite.idwritefontface3_getpanose","dwrite_3/IDWriteFontFace3::GetPanose"]
old-location: directwrite\idwritefontface3_getpanose.htm
tech.root: DirectWrite
ms.assetid: 977AFC97-9747-4FCE-861E-E1C40975B2E9
ms.date: 09/10/2025
ms.keywords: GetPanose, GetPanose method [Direct Write], GetPanose method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetPanose method, IDWriteFontFace3.GetPanose, IDWriteFontFace3::GetPanose, directwrite.idwritefontface3_getpanose, dwrite_3/IDWriteFontFace3::GetPanose
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
 - IDWriteFontFace3::GetPanose
 - dwrite_3/IDWriteFontFace3::GetPanose
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
 - IDWriteFontFace3.GetPanose
---

# IDWriteFontFace3::GetPanose


## -description

Gets the PANOSE values from the font, used for font selection and matching.

## -parameters

### -param panose [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose">DWRITE_PANOSE</a>*</b>

A pointer to a <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose">DWRITE_PANOSE</a> structure that receives the PANOSE values from the font.

## -remarks

This method doesn't simulate these values, such as substituting a weight or proportion inferred on other values. If the font doesn't specify them, they are all set to 'any' (0).

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

