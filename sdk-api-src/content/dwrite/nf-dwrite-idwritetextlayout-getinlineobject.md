---
UID: NF:dwrite.IDWriteTextLayout.GetInlineObject
title: IDWriteTextLayout::GetInlineObject (dwrite.h)
description: Gets the inline object at the specified position.
helpviewer_keywords: ["GetInlineObject","GetInlineObject method [Direct Write]","GetInlineObject method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetInlineObject method","IDWriteTextLayout.GetInlineObject","IDWriteTextLayout::GetInlineObject","directwrite.IDWriteTextLayout_GetInlineObject","dwrite/IDWriteTextLayout::GetInlineObject"]
old-location: directwrite\IDWriteTextLayout_GetInlineObject.htm
tech.root: DirectWrite
ms.assetid: 0d86f2a4-d046-4d27-b128-40f2a3dd359a
ms.date: 12/05/2018
ms.keywords: GetInlineObject, GetInlineObject method [Direct Write], GetInlineObject method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetInlineObject method, IDWriteTextLayout.GetInlineObject, IDWriteTextLayout::GetInlineObject, directwrite.IDWriteTextLayout_GetInlineObject, dwrite/IDWriteTextLayout::GetInlineObject
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
 - IDWriteTextLayout::GetInlineObject
 - dwrite/IDWriteTextLayout::GetInlineObject
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
 - IDWriteTextLayout.GetInlineObject
---

# IDWriteTextLayout::GetInlineObject


## -description

 Gets the inline object at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The specified text position.

### -param inlineObject [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>**</b>

Contains the application-defined inline object.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the inline object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

