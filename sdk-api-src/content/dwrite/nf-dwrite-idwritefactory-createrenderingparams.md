---
UID: NF:dwrite.IDWriteFactory.CreateRenderingParams
title: IDWriteFactory::CreateRenderingParams (dwrite.h)
description: Creates a rendering parameters object with default settings for the primary monitor. Different monitors may have different rendering parameters, for more information see the How to Add Support for Multiple Monitors topic.
helpviewer_keywords: ["CreateRenderingParams","CreateRenderingParams method [Direct Write]","CreateRenderingParams method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateRenderingParams method","IDWriteFactory.CreateRenderingParams","IDWriteFactory::CreateRenderingParams","directwrite.IDWriteFactory_CreateRenderingParams","dwrite/IDWriteFactory::CreateRenderingParams"]
old-location: directwrite\IDWriteFactory_CreateRenderingParams.htm
tech.root: DirectWrite
ms.assetid: f5e3e609-62ee-4a0a-aed1-591be852590e
ms.date: 12/05/2018
ms.keywords: CreateRenderingParams, CreateRenderingParams method [Direct Write], CreateRenderingParams method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateRenderingParams method, IDWriteFactory.CreateRenderingParams, IDWriteFactory::CreateRenderingParams, directwrite.IDWriteFactory_CreateRenderingParams, dwrite/IDWriteFactory::CreateRenderingParams
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
 - IDWriteFactory::CreateRenderingParams
 - dwrite/IDWriteFactory::CreateRenderingParams
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
 - IDWriteFactory.CreateRenderingParams
---

# IDWriteFactory::CreateRenderingParams


## -description

 Creates a rendering parameters object with default settings for the primary monitor.
    Different monitors may have different rendering parameters, for more information see the <a href="/windows/win32/DirectWrite/how-to-add-support-for-multiple-monitors">How to Add Support for Multiple Monitors</a> topic.

## -parameters

### -param renderingParams [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>**</b>

When this method returns, contains an address of a pointer to the newly created  rendering parameters object.

## -returns

Type: <b>HRESULT</b>

Standard HRESULT error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>



<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams">IDWriteFactory::CreateMonitorRenderingParams</a>

