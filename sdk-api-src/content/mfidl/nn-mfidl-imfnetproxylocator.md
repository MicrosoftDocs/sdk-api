---
UID: NN:mfidl.IMFNetProxyLocator
title: IMFNetProxyLocator
author: windows-sdk-content
description: Determines the proxy to use when connecting to a server.
old-location: mf\imfnetproxylocator.htm
tech.root: medfound
ms.assetid: 2906b998-f1ca-4c65-b810-cbc360390653
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 2906b998-f1ca-4c65-b810-cbc360390653, IMFNetProxyLocator, IMFNetProxyLocator interface [Media Foundation], IMFNetProxyLocator interface [Media Foundation],described, mf.imfnetproxylocator, mfidl/IMFNetProxyLocator
ms.prod: windows
ms.technology: windows-sdk
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
---

# IMFNetProxyLocator interface


## -description


Determines the proxy to use when connecting to a server. The network source uses this interface.

Applications can create the proxy locator configured by the application by implementing the <a href="https://msdn.microsoft.com/6dd5bf50-2d07-47c7-869e-035d7e92a6bc">IMFNetProxyLocatorFactory</a> interface and setting the <a href="https://msdn.microsoft.com/455325c0-5116-4e81-9729-fab9c6a367c7">MFNETSOURCE_PROXYLOCATORFACTORY</a> property on the source resolver. Otherwise, the network source uses the default Media Foundation implementation.

To create the default proxy locator, call <a href="https://msdn.microsoft.com/9ad707df-533a-407b-a611-49bfb019affc">MFCreateProxyLocator</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetProxyLocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetProxyLocator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/551372b3-b9aa-4057-8c14-19e582053e00">Clone</a>
</td>
<td align="left" width="63%">
Creates a new instance of the proxy locator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48eba170-eeed-4edf-b8d3-2f4541637129">FindFirstProxy</a>
</td>
<td align="left" width="63%">
Initializes the proxy locator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91a6046f-f5c3-4239-af71-d25e9d5b5838">FindNextProxy</a>
</td>
<td align="left" width="63%">
Determines the next proxy to use in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bc9a87b-a6d5-4ae0-a3a2-9cef2df79272">GetCurrentProxy</a>
</td>
<td align="left" width="63%">
Retrieves the current proxy information including hostname and port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b1a55c6-7d78-47cc-9098-6504d11a4eef">RegisterProxyResult</a>
</td>
<td align="left" width="63%">
Keeps record of the success or failure of using the current proxy.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/e739746d-2a09-4237-a7c1-0aed4e4516d7">Proxy Support for Network Sources</a>
 

 

