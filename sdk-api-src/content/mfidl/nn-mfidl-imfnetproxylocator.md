---
UID: NN:mfidl.IMFNetProxyLocator
title: IMFNetProxyLocator (mfidl.h)
author: windows-sdk-content
description: Determines the proxy to use when connecting to a server.
old-location: mf\imfnetproxylocator.htm
tech.root: medfound
ms.assetid: 2906b998-f1ca-4c65-b810-cbc360390653
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2906b998-f1ca-4c65-b810-cbc360390653, IMFNetProxyLocator, IMFNetProxyLocator interface [Media Foundation], IMFNetProxyLocator interface [Media Foundation],described, mf.imfnetproxylocator, mfidl/IMFNetProxyLocator
ms.topic: interface
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
 - IMFNetProxyLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetProxyLocator interface


## -description


Determines the proxy to use when connecting to a server. The network source uses this interface.

Applications can create the proxy locator configured by the application by implementing the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory">IMFNetProxyLocatorFactory</a> interface and setting the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfnetsource-proxylocatorfactory-property">MFNETSOURCE_PROXYLOCATORFACTORY</a> property on the source resolver. Otherwise, the network source uses the default Media Foundation implementation.

To create the default proxy locator, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator">MFCreateProxyLocator</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetProxyLocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetProxyLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetProxyLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocator-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new instance of the proxy locator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocator-findfirstproxy">FindFirstProxy</a>
</td>
<td align="left" width="63%">
Initializes the proxy locator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocator-findnextproxy">FindNextProxy</a>
</td>
<td align="left" width="63%">
Determines the next proxy to use in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocator-getcurrentproxy">GetCurrentProxy</a>
</td>
<td align="left" width="63%">
Retrieves the current proxy information including hostname and port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocator-registerproxyresult">RegisterProxyResult</a>
</td>
<td align="left" width="63%">
Keeps record of the success or failure of using the current proxy.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/proxy-support-for-network-sources">Proxy Support for Network Sources</a>
 

 

