---
UID: NF:dwrite.IDWriteTextLayout.SetUnderline
title: IDWriteTextLayout::SetUnderline (dwrite.h)
description: Sets underlining for text within a specified text range.
helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetUnderline method","IDWriteTextLayout.SetUnderline","IDWriteTextLayout::SetUnderline","SetUnderline","SetUnderline method [Direct Write]","SetUnderline method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetUnderline","dwrite/IDWriteTextLayout::SetUnderline"]
old-location: directwrite\IDWriteTextLayout_SetUnderline.htm
tech.root: DirectWrite
ms.assetid: 677bb4e2-4ae9-4e79-96a3-d4961e317886
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetUnderline method, IDWriteTextLayout.SetUnderline, IDWriteTextLayout::SetUnderline, SetUnderline, SetUnderline method [Direct Write], SetUnderline method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetUnderline, dwrite/IDWriteTextLayout::SetUnderline
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
 - IDWriteTextLayout::SetUnderline
 - dwrite/IDWriteTextLayout::SetUnderline
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
 - IDWriteTextLayout.SetUnderline
---

# IDWriteTextLayout::SetUnderline


## -description

Sets underlining for text within a specified text range.

## -parameters

### -param hasUnderline

Type: <b>BOOL</b>

A Boolean flag that indicates whether underline takes place within a specified text range.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

