---
UID: NF:dwrite_1.IDWriteFont1.GetPanose
title: IDWriteFont1::GetPanose (dwrite_1.h)
description: Gets the PANOSE values from the font and is used for font selection and matching.
helpviewer_keywords: ["GetPanose","GetPanose method [Direct Write]","GetPanose method [Direct Write]","IDWriteFont1 interface","IDWriteFont1 interface [Direct Write]","GetPanose method","IDWriteFont1.GetPanose","IDWriteFont1::GetPanose","directwrite.idwritefont1_getpanose","dwrite_1/IDWriteFont1::GetPanose"]
old-location: directwrite\idwritefont1_getpanose.htm
tech.root: DirectWrite
ms.assetid: DD31C1D6-4CD2-4ED0-BF9F-CAF587C613E6
ms.date: 12/05/2018
ms.keywords: GetPanose, GetPanose method [Direct Write], GetPanose method [Direct Write],IDWriteFont1 interface, IDWriteFont1 interface [Direct Write],GetPanose method, IDWriteFont1.GetPanose, IDWriteFont1::GetPanose, directwrite.idwritefont1_getpanose, dwrite_1/IDWriteFont1::GetPanose
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFont1::GetPanose
 - dwrite_1/IDWriteFont1::GetPanose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFont1.GetPanose
---

# IDWriteFont1::GetPanose


## -description

Gets the PANOSE values from the font and is used for font selection and
    matching.

## -parameters

### -param panose [out]

Type: <b><a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose">DWRITE_PANOSE</a>*</b>

A pointer to the <a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose">DWRITE_PANOSE</a> structure to fill in.

## -remarks

If the font has no PANOSE values,
    they are set to 'any' (0) and <a href="/windows/win32/DirectWrite/direct-write-portal">DirectWrite</a> doesn't simulate those values.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1">IDWriteFont1</a>

