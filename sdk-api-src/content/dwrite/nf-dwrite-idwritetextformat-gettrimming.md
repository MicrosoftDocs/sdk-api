---
UID: NF:dwrite.IDWriteTextFormat.GetTrimming
title: IDWriteTextFormat::GetTrimming (dwrite.h)
description: Gets the trimming options for text that overflows the layout box.
helpviewer_keywords: ["GetTrimming","GetTrimming method [Direct Write]","GetTrimming method [Direct Write]","IDWriteTextFormat interface","IDWriteTextFormat interface [Direct Write]","GetTrimming method","IDWriteTextFormat.GetTrimming","IDWriteTextFormat::GetTrimming","directwrite.IDWriteTextFormat_GetTrimming","dwrite/IDWriteTextFormat::GetTrimming"]
old-location: directwrite\IDWriteTextFormat_GetTrimming.htm
tech.root: DirectWrite
ms.assetid: 6147d0a4-8f50-40c6-864e-734cfef57089
ms.date: 12/05/2018
ms.keywords: GetTrimming, GetTrimming method [Direct Write], GetTrimming method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetTrimming method, IDWriteTextFormat.GetTrimming, IDWriteTextFormat::GetTrimming, directwrite.IDWriteTextFormat_GetTrimming, dwrite/IDWriteTextFormat::GetTrimming
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextFormat::GetTrimming
 - dwrite/IDWriteTextFormat::GetTrimming
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
 - IDWriteTextFormat.GetTrimming
---

# IDWriteTextFormat::GetTrimming


## -description

 Gets the trimming options for text that overflows the layout box.

## -parameters

### -param trimmingOptions [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming">DWRITE_TRIMMING</a>*</b>

When this method returns, it contains a pointer to a <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming">DWRITE_TRIMMING</a> structure that holds the text trimming options for the overflowing text.

### -param trimmingSign [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>**</b>

When this method returns, contains an address of a pointer to a trimming omission sign. This parameter may be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

