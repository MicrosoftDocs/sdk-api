---
UID: NN:mfidl.IMFNetProxyLocatorFactory
title: IMFNetProxyLocatorFactory (mfidl.h)
description: Creates a proxy locator object, which determines the proxy to use.
helpviewer_keywords: ["6dd5bf50-2d07-47c7-869e-035d7e92a6bc","IMFNetProxyLocatorFactory","IMFNetProxyLocatorFactory interface [Media Foundation]","IMFNetProxyLocatorFactory interface [Media Foundation]","described","mf.imfnetproxylocatorfactory","mfidl/IMFNetProxyLocatorFactory"]
old-location: mf\imfnetproxylocatorfactory.htm
tech.root: mf
ms.assetid: 6dd5bf50-2d07-47c7-869e-035d7e92a6bc
ms.date: 12/05/2018
ms.keywords: 6dd5bf50-2d07-47c7-869e-035d7e92a6bc, IMFNetProxyLocatorFactory, IMFNetProxyLocatorFactory interface [Media Foundation], IMFNetProxyLocatorFactory interface [Media Foundation],described, mf.imfnetproxylocatorfactory, mfidl/IMFNetProxyLocatorFactory
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetProxyLocatorFactory
 - mfidl/IMFNetProxyLocatorFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetProxyLocatorFactory
---

# IMFNetProxyLocatorFactory interface


## -description

Creates a proxy locator object, which determines the proxy to use.

The network source uses this interface to create the proxy locator object. Applications can provide their own implementation of this interface by setting the <a href="/windows/desktop/medfound/mfnetsource-proxylocatorfactory-property">MFNETSOURCE_PROXYLOCATORFACTORY</a> property. on the source resolver. If the application does not set this property, the network source uses the default proxy locator provided by Media Foundation.

## -inheritance

The <b>IMFNetProxyLocatorFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetProxyLocatorFactory</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/how-to-configure-the-proxy-locator">How to Configure the Proxy Locator</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
