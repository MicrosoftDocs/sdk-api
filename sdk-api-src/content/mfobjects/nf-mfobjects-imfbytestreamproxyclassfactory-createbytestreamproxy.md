---
UID: NF:mfobjects.IMFByteStreamProxyClassFactory.CreateByteStreamProxy
title: IMFByteStreamProxyClassFactory::CreateByteStreamProxy
author: windows-sdk-content
description: Creates a proxy to a byte stream.
old-location: mf\imfbytestreamproxyclassfactory_createbytestreamproxy.htm
old-project: medfound
ms.assetid: 5A7E6218-615F-43E3-BB96-0D39138A4E28
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CreateByteStreamProxy, CreateByteStreamProxy method [Media Foundation], CreateByteStreamProxy method [Media Foundation],IMFByteStreamProxyClassFactory interface, IMFByteStreamProxyClassFactory interface [Media Foundation],CreateByteStreamProxy method, IMFByteStreamProxyClassFactory.CreateByteStreamProxy, IMFByteStreamProxyClassFactory::CreateByteStreamProxy, mf.imfbytestreamproxyclassfactory_createbytestreamproxy, mfobjects/IMFByteStreamProxyClassFactory::CreateByteStreamProxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFByteStreamProxyClassFactory.CreateByteStreamProxy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamProxyClassFactory::CreateByteStreamProxy


## -description


Creates a proxy to a byte stream. The proxy enables a media source to read from a byte stream in another process.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the byte stream to proxy.


### -param pAttributes [in]

Reserved. Set to <b>NULL</b>.


### -param riid [in]

The interface identifer (IID) of the interface being requested.


### -param ppvObject [out]

Receives a pointer to the interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/DF29B5FC-864F-4400-8EDB-3A2CD797E37A">IMFByteStreamProxyClassFactory</a>
 

 

