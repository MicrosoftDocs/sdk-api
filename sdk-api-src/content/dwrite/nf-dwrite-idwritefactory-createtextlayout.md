---
UID: NF:dwrite.IDWriteFactory.CreateTextLayout
title: IDWriteFactory::CreateTextLayout (dwrite.h)
description: Takes a string, text format, and associated constraints, and produces an object that represents the fully analyzed and formatted result.
helpviewer_keywords: ["CreateTextLayout","CreateTextLayout method [Direct Write]","CreateTextLayout method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateTextLayout method","IDWriteFactory.CreateTextLayout","IDWriteFactory::CreateTextLayout","directwrite.IDWriteFactory_CreateTextLayout","dwrite/IDWriteFactory::CreateTextLayout"]
old-location: directwrite\IDWriteFactory_CreateTextLayout.htm
tech.root: DirectWrite
ms.assetid: f76f85df-112f-4bc3-b922-a0d7940d2954
ms.date: 12/05/2018
ms.keywords: CreateTextLayout, CreateTextLayout method [Direct Write], CreateTextLayout method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTextLayout method, IDWriteFactory.CreateTextLayout, IDWriteFactory::CreateTextLayout, directwrite.IDWriteFactory_CreateTextLayout, dwrite/IDWriteFactory::CreateTextLayout
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
 - IDWriteFactory::CreateTextLayout
 - dwrite/IDWriteFactory::CreateTextLayout
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
 - IDWriteFactory.CreateTextLayout
---

# IDWriteFactory::CreateTextLayout


## -description

 Takes a string, text format, and associated constraints,
     and produces an object that represents the fully analyzed
     and formatted result.

## -parameters

### -param string [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the string to create a new <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> object from. This array must be of length <i>stringLength</i> and can contain embedded <b>NULL</b> characters.

### -param stringLength

Type: <b>UINT32</b>

The number of characters in  the string.

### -param textFormat

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>*</b>

A pointer to an object that indicates the format to apply to the string.

### -param maxWidth

Type: <b>FLOAT</b>

The width of the layout box.

### -param maxHeight

Type: <b>FLOAT</b>

The height of the layout box.

### -param textLayout [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>**</b>

When this method returns, contains an address of a pointer to the resultant text layout object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

