---
UID: NF:dwrite.IDWriteTextLayout.GetFontSize
title: IDWriteTextLayout::GetFontSize (dwrite.h)
description: Gets the font em height of the text at the specified position.
helpviewer_keywords: ["GetFontSize","GetFontSize method [Direct Write]","GetFontSize method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontSize method","IDWriteTextLayout.GetFontSize","IDWriteTextLayout::GetFontSize","directwrite.IDWriteTextLayout_GetFontSize","dwrite/IDWriteTextLayout::GetFontSize"]
old-location: directwrite\IDWriteTextLayout_GetFontSize.htm
tech.root: DirectWrite
ms.assetid: 31cf375a-d749-4af1-9470-73439fe6276e
ms.date: 12/05/2018
ms.keywords: GetFontSize, GetFontSize method [Direct Write], GetFontSize method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontSize method, IDWriteTextLayout.GetFontSize, IDWriteTextLayout::GetFontSize, directwrite.IDWriteTextLayout_GetFontSize, dwrite/IDWriteTextLayout::GetFontSize
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
 - IDWriteTextLayout::GetFontSize
 - dwrite/IDWriteTextLayout::GetFontSize
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
 - IDWriteTextLayout.GetFontSize
---

# IDWriteTextLayout::GetFontSize


## -description

 Gets the font em height of the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.

### -param fontSize [out]

Type: <b>FLOAT*</b>

When this method returns, contains the size of the font in ems  of the text at the specified position.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font size.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

