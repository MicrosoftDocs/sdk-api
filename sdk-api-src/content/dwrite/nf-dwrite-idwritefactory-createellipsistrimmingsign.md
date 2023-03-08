---
UID: NF:dwrite.IDWriteFactory.CreateEllipsisTrimmingSign
title: IDWriteFactory::CreateEllipsisTrimmingSign (dwrite.h)
description: Creates an inline object for trimming, using an ellipsis as the omission sign.
helpviewer_keywords: ["CreateEllipsisTrimmingSign","CreateEllipsisTrimmingSign method [Direct Write]","CreateEllipsisTrimmingSign method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateEllipsisTrimmingSign method","IDWriteFactory.CreateEllipsisTrimmingSign","IDWriteFactory::CreateEllipsisTrimmingSign","directwrite.IDWriteFactory_CreateEllipsisTrimmingSign","dwrite/IDWriteFactory::CreateEllipsisTrimmingSign"]
old-location: directwrite\IDWriteFactory_CreateEllipsisTrimmingSign.htm
tech.root: DirectWrite
ms.assetid: b416d9f7-d2ce-477c-bf03-b20da2a55bb6
ms.date: 12/05/2018
ms.keywords: CreateEllipsisTrimmingSign, CreateEllipsisTrimmingSign method [Direct Write], CreateEllipsisTrimmingSign method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateEllipsisTrimmingSign method, IDWriteFactory.CreateEllipsisTrimmingSign, IDWriteFactory::CreateEllipsisTrimmingSign, directwrite.IDWriteFactory_CreateEllipsisTrimmingSign, dwrite/IDWriteFactory::CreateEllipsisTrimmingSign
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
 - IDWriteFactory::CreateEllipsisTrimmingSign
 - dwrite/IDWriteFactory::CreateEllipsisTrimmingSign
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
 - IDWriteFactory.CreateEllipsisTrimmingSign
---

# IDWriteFactory::CreateEllipsisTrimmingSign


## -description

 Creates an inline object for trimming, using an ellipsis as the omission sign.

## -parameters

### -param textFormat

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>*</b>

A text format object, created with <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat">CreateTextFormat</a>, used for text layout.

### -param trimmingSign [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>**</b>

When this method returns, contains an address of a pointer to the omission (that is, ellipsis trimming) sign created by this method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The ellipsis will be created using the current settings of the format, including base font, style, and any effects.
     Alternate omission signs can be created by the application by implementing <a href="/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

