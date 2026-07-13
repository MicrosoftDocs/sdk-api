---
UID: NF:dwrite.IDWriteTextFormat.GetLineSpacing
title: IDWriteTextFormat::GetLineSpacing (dwrite.h)
description: Gets the line spacing adjustment set for a multiline text paragraph. (IDWriteTextFormat.GetLineSpacing)
helpviewer_keywords: ["GetLineSpacing","GetLineSpacing method [Direct Write]","GetLineSpacing method [Direct Write]","IDWriteTextFormat interface","IDWriteTextFormat interface [Direct Write]","GetLineSpacing method","IDWriteTextFormat.GetLineSpacing","IDWriteTextFormat::GetLineSpacing","directwrite.IDWriteTextFormat_GetLineSpacing","dwrite/IDWriteTextFormat::GetLineSpacing"]
old-location: directwrite\IDWriteTextFormat_GetLineSpacing.htm
tech.root: DirectWrite
ms.assetid: d9563d4d-0b7d-4921-b251-6ef1e24105f1
ms.date: 12/05/2018
ms.keywords: GetLineSpacing, GetLineSpacing method [Direct Write], GetLineSpacing method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetLineSpacing method, IDWriteTextFormat.GetLineSpacing, IDWriteTextFormat::GetLineSpacing, directwrite.IDWriteTextFormat_GetLineSpacing, dwrite/IDWriteTextFormat::GetLineSpacing
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
 - IDWriteTextFormat::GetLineSpacing
 - dwrite/IDWriteTextFormat::GetLineSpacing
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
 - IDWriteTextFormat.GetLineSpacing
---

# IDWriteTextFormat::GetLineSpacing


## -description

 Gets the line spacing adjustment set for a multiline text paragraph.

## -parameters

### -param lineSpacingMethod [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method">DWRITE_LINE_SPACING_METHOD</a>*</b>

A value that indicates how line height is determined.

### -param lineSpacing [out]

Type: <b>FLOAT*</b>

When this method returns, contains the line height, or  distance between one baseline to another.

### -param baseline [out]

Type: <b>FLOAT*</b>

When this method returns, contains the distance from top of line to baseline. A reasonable ratio to <i>lineSpacing</i> is 80 percent.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

