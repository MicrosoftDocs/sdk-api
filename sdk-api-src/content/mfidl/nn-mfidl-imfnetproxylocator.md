---
UID: NN:mfidl.IMFNetProxyLocator
title: IMFNetProxyLocator (mfidl.h)
description: Determines the proxy to use when connecting to a server.
helpviewer_keywords: ["2906b998-f1ca-4c65-b810-cbc360390653","IMFNetProxyLocator","IMFNetProxyLocator interface [Media Foundation]","IMFNetProxyLocator interface [Media Foundation]","described","mf.imfnetproxylocator","mfidl/IMFNetProxyLocator"]
old-location: mf\imfnetproxylocator.htm
tech.root: mf
ms.assetid: 2906b998-f1ca-4c65-b810-cbc360390653
ms.date: 12/05/2018
ms.keywords: 2906b998-f1ca-4c65-b810-cbc360390653, IMFNetProxyLocator, IMFNetProxyLocator interface [Media Foundation], IMFNetProxyLocator interface [Media Foundation],described, mf.imfnetproxylocator, mfidl/IMFNetProxyLocator
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
 - IMFNetProxyLocator
 - mfidl/IMFNetProxyLocator
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
 - IMFNetProxyLocator
---

# IMFNetProxyLocator interface


## -description

Determines the proxy to use when connecting to a server. The network source uses this interface.

Applications can create the proxy locator configured by the application by implementing the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory">IMFNetProxyLocatorFactory</a> interface and setting the <a href="/windows/desktop/medfound/mfnetsource-proxylocatorfactory-property">MFNETSOURCE_PROXYLOCATORFACTORY</a> property on the source resolver. Otherwise, the network source uses the default Media Foundation implementation.

To create the default proxy locator, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator">MFCreateProxyLocator</a>.

## -inheritance

The <b>IMFNetProxyLocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetProxyLocator</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/proxy-support-for-network-sources">Proxy Support for Network Sources</a>
