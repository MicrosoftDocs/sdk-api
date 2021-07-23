---
UID: NF:dwrite.IDWriteFactory.CreateTypography
title: IDWriteFactory::CreateTypography (dwrite.h)
description: Creates a typography object for use in a text layout.
helpviewer_keywords: ["CreateTypography","CreateTypography method [Direct Write]","CreateTypography method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateTypography method","IDWriteFactory.CreateTypography","IDWriteFactory::CreateTypography","directwrite.IDWriteFactory_CreateTypography","dwrite/IDWriteFactory::CreateTypography"]
old-location: directwrite\IDWriteFactory_CreateTypography.htm
tech.root: DirectWrite
ms.assetid: ef6d8289-3a8a-4ec1-89a8-b1b52e311d63
ms.date: 12/05/2018
ms.keywords: CreateTypography, CreateTypography method [Direct Write], CreateTypography method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTypography method, IDWriteFactory.CreateTypography, IDWriteFactory::CreateTypography, directwrite.IDWriteFactory_CreateTypography, dwrite/IDWriteFactory::CreateTypography
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
 - IDWriteFactory::CreateTypography
 - dwrite/IDWriteFactory::CreateTypography
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
 - IDWriteFactory.CreateTypography
---

# IDWriteFactory::CreateTypography


## -description

 Creates a typography object for use in a text layout.

## -parameters

### -param typography [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetypography">IDWriteTypography</a>**</b>

When this method returns, contains the address of  a pointer to a newly created typography object, or <b>NULL</b> in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

