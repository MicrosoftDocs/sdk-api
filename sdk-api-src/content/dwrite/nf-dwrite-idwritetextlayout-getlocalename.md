---
UID: NF:dwrite.IDWriteTextLayout.GetLocaleName
title: IDWriteTextLayout::GetLocaleName (dwrite.h)
description: Gets the locale name of the text at the specified position.
helpviewer_keywords: ["GetLocaleName","GetLocaleName method [Direct Write]","GetLocaleName method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetLocaleName method","IDWriteTextLayout.GetLocaleName","IDWriteTextLayout::GetLocaleName","directwrite.IDWriteTextLayout_GetLocaleName","dwrite/IDWriteTextLayout::GetLocaleName"]
old-location: directwrite\IDWriteTextLayout_GetLocaleName.htm
tech.root: DirectWrite
ms.assetid: 6d0c0609-f568-41cd-9d3f-37ff92174e29
ms.date: 12/05/2018
ms.keywords: GetLocaleName, GetLocaleName method [Direct Write], GetLocaleName method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetLocaleName method, IDWriteTextLayout.GetLocaleName, IDWriteTextLayout::GetLocaleName, directwrite.IDWriteTextLayout_GetLocaleName, dwrite/IDWriteTextLayout::GetLocaleName
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
 - IDWriteTextLayout::GetLocaleName
 - dwrite/IDWriteTextLayout::GetLocaleName
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
 - IDWriteTextLayout.GetLocaleName
---

# IDWriteTextLayout::GetLocaleName


## -description

 Gets the locale name of the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.

### -param localeName [out]

Type: <b>WCHAR*</b>

When this method returns, contains the character array receiving the current locale name.

### -param nameSize

Type: <b>UINT32</b>

Size of the character array, in character count, including the terminated <b>NULL</b> character.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the locale name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

