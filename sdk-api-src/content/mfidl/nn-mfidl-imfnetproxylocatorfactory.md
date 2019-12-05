---
UID: NN:mfidl.IMFNetProxyLocatorFactory
title: IMFNetProxyLocatorFactory (mfidl.h)
description: Creates a proxy locator object, which determines the proxy to use.
old-location: mf\imfnetproxylocatorfactory.htm
tech.root: medfound
ms.assetid: 6dd5bf50-2d07-47c7-869e-035d7e92a6bc
ms.date: 12/05/2018
ms.keywords: 6dd5bf50-2d07-47c7-869e-035d7e92a6bc, IMFNetProxyLocatorFactory, IMFNetProxyLocatorFactory interface [Media Foundation], IMFNetProxyLocatorFactory interface [Media Foundation],described, mf.imfnetproxylocatorfactory, mfidl/IMFNetProxyLocatorFactory
ms.topic: interface
f1_keywords:
- mfidl/IMFNetProxyLocatorFactory
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetProxyLocatorFactory interface


## -description


Creates a proxy locator object, which determines the proxy to use.

The network source uses this interface to create the proxy locator object. Applications can provide their own implementation of this interface by setting the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfnetsource-proxylocatorfactory-property">MFNETSOURCE_PROXYLOCATORFACTORY</a> property. on the source resolver. If the application does not set this property, the network source uses the default proxy locator provided by Media Foundation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetProxyLocatorFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetProxyLocatorFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetProxyLocatorFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator">CreateProxyLocator</a>
</td>
<td align="left" width="63%">
Creates a proxy locator object based on the protocol name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-configure-the-proxy-locator">How to Configure the Proxy Locator</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

