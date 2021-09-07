---
UID: NF:dwrite.IDWriteFactory.CreateMonitorRenderingParams
title: IDWriteFactory::CreateMonitorRenderingParams (dwrite.h)
description: Creates a rendering parameters object with default settings for the specified monitor. In most cases, this is the preferred way to create a rendering parameters object.
helpviewer_keywords: ["CreateMonitorRenderingParams","CreateMonitorRenderingParams method [Direct Write]","CreateMonitorRenderingParams method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateMonitorRenderingParams method","IDWriteFactory.CreateMonitorRenderingParams","IDWriteFactory::CreateMonitorRenderingParams","directwrite.IDWriteFactory_CreateMonitorRenderingParams","dwrite/IDWriteFactory::CreateMonitorRenderingParams"]
old-location: directwrite\IDWriteFactory_CreateMonitorRenderingParams.htm
tech.root: DirectWrite
ms.assetid: ddb6839a-9033-423a-a3f0-9352ec03e440
ms.date: 12/05/2018
ms.keywords: CreateMonitorRenderingParams, CreateMonitorRenderingParams method [Direct Write], CreateMonitorRenderingParams method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateMonitorRenderingParams method, IDWriteFactory.CreateMonitorRenderingParams, IDWriteFactory::CreateMonitorRenderingParams, directwrite.IDWriteFactory_CreateMonitorRenderingParams, dwrite/IDWriteFactory::CreateMonitorRenderingParams
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
 - IDWriteFactory::CreateMonitorRenderingParams
 - dwrite/IDWriteFactory::CreateMonitorRenderingParams
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
 - IDWriteFactory.CreateMonitorRenderingParams
---

# IDWriteFactory::CreateMonitorRenderingParams


## -description

 Creates a rendering parameters object with default settings for the specified monitor.
    In most cases, this is the preferred way to create a rendering parameters object.

## -parameters

### -param monitor

Type: <b>HMONITOR</b>

A handle for the specified monitor.

### -param renderingParams [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>**</b>

When this method returns, contains an address of a pointer to the rendering parameters object created by this method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

