---
UID: NN:mfidl.IMFRemoteProxy
title: IMFRemoteProxy
author: windows-sdk-content
description: Exposed by objects that act as a proxy for a remote object.
old-location: mf\imfremoteproxy.htm
tech.root: MedFound
ms.assetid: 46af5ba7-c362-4cfd-ae6d-b698c6403a65
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 46af5ba7-c362-4cfd-ae6d-b698c6403a65, IMFRemoteProxy, IMFRemoteProxy interface [Media Foundation], IMFRemoteProxy interface [Media Foundation],described, mf.imfremoteproxy, mfidl/IMFRemoteProxy
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
 - IMFRemoteProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFRemoteProxy interface


## -description


Exposed by objects that act as a proxy for a remote object. To obtain a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MF_REMOTE_PROXY.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRemoteProxy</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFRemoteProxy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRemoteProxy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3a4407a-d8e4-4c7b-81da-88d63e0d77b8">GetRemoteHost</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object that is hosting this proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d9e35bd-fe4c-4a98-91c8-2192ae34b2b3">GetRemoteObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the remote object for which this object is a proxy.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>
 

 

