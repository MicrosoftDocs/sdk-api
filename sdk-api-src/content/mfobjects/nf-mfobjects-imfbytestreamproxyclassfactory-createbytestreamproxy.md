---
UID: NF:mfobjects.IMFByteStreamProxyClassFactory.CreateByteStreamProxy
title: IMFByteStreamProxyClassFactory::CreateByteStreamProxy (mfobjects.h)
description: Creates a proxy to a byte stream. (IMFByteStreamProxyClassFactory.CreateByteStreamProxy)
helpviewer_keywords: ["CreateByteStreamProxy","CreateByteStreamProxy method [Media Foundation]","CreateByteStreamProxy method [Media Foundation]","IMFByteStreamProxyClassFactory interface","IMFByteStreamProxyClassFactory interface [Media Foundation]","CreateByteStreamProxy method","IMFByteStreamProxyClassFactory.CreateByteStreamProxy","IMFByteStreamProxyClassFactory::CreateByteStreamProxy","mf.imfbytestreamproxyclassfactory_createbytestreamproxy","mfobjects/IMFByteStreamProxyClassFactory::CreateByteStreamProxy"]
old-location: mf\imfbytestreamproxyclassfactory_createbytestreamproxy.htm
tech.root: mf
ms.assetid: 5A7E6218-615F-43E3-BB96-0D39138A4E28
ms.date: 12/05/2018
ms.keywords: CreateByteStreamProxy, CreateByteStreamProxy method [Media Foundation], CreateByteStreamProxy method [Media Foundation],IMFByteStreamProxyClassFactory interface, IMFByteStreamProxyClassFactory interface [Media Foundation],CreateByteStreamProxy method, IMFByteStreamProxyClassFactory.CreateByteStreamProxy, IMFByteStreamProxyClassFactory::CreateByteStreamProxy, mf.imfbytestreamproxyclassfactory_createbytestreamproxy, mfobjects/IMFByteStreamProxyClassFactory::CreateByteStreamProxy
req.header: mfobjects.h
req.include-header: Mfidl.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamProxyClassFactory::CreateByteStreamProxy
 - mfobjects/IMFByteStreamProxyClassFactory::CreateByteStreamProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFByteStreamProxyClassFactory.CreateByteStreamProxy
---

# IMFByteStreamProxyClassFactory::CreateByteStreamProxy


## -description

Creates a proxy to a byte stream. The proxy enables a media source to read from a byte stream in another process.

## -parameters

### -param pByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the byte stream to proxy.

### -param pAttributes [in]

Reserved. Set to <b>NULL</b>.

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppvObject [out]

Receives a pointer to the interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestreamproxyclassfactory">IMFByteStreamProxyClassFactory</a>
