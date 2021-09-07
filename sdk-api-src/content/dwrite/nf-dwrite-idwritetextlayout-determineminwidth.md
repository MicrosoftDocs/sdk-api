---
UID: NF:dwrite.IDWriteTextLayout.DetermineMinWidth
title: IDWriteTextLayout::DetermineMinWidth (dwrite.h)
description: Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.
helpviewer_keywords: ["DetermineMinWidth","DetermineMinWidth method [Direct Write]","DetermineMinWidth method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","DetermineMinWidth method","IDWriteTextLayout.DetermineMinWidth","IDWriteTextLayout::DetermineMinWidth","directwrite.idwritetextlayout_determineminwidth","dwrite/IDWriteTextLayout::DetermineMinWidth"]
old-location: directwrite\idwritetextlayout_determineminwidth.htm
tech.root: DirectWrite
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
ms.date: 12/05/2018
ms.keywords: DetermineMinWidth, DetermineMinWidth method [Direct Write], DetermineMinWidth method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],DetermineMinWidth method, IDWriteTextLayout.DetermineMinWidth, IDWriteTextLayout::DetermineMinWidth, directwrite.idwritetextlayout_determineminwidth, dwrite/IDWriteTextLayout::DetermineMinWidth
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteTextLayout::DetermineMinWidth
 - dwrite/IDWriteTextLayout::DetermineMinWidth
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
 - IDWriteTextLayout.DetermineMinWidth
---

# IDWriteTextLayout::DetermineMinWidth


## -description

Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.

## -parameters

### -param minWidth [out]

Type: <b>FLOAT*</b>

Minimum width.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

