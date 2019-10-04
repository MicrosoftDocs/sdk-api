---
UID: NN:mfidl.IMFRemoteProxy
title: IMFRemoteProxy (mfidl.h)
author: windows-sdk-content
description: Exposed by objects that act as a proxy for a remote object.
old-location: mf\imfremoteproxy.htm
tech.root: medfound
ms.assetid: 46af5ba7-c362-4cfd-ae6d-b698c6403a65
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 46af5ba7-c362-4cfd-ae6d-b698c6403a65, IMFRemoteProxy, IMFRemoteProxy interface [Media Foundation], IMFRemoteProxy interface [Media Foundation],described, mf.imfremoteproxy, mfidl/IMFRemoteProxy
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFRemoteProxy"
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
 - IMFRemoteProxy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFRemoteProxy interface


## -description


Exposed by objects that act as a proxy for a remote object. To obtain a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MF_REMOTE_PROXY.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRemoteProxy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRemoteProxy</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfremoteproxy-getremotehost">GetRemoteHost</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object that is hosting this proxy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfremoteproxy-getremoteobject">GetRemoteObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the remote object for which this object is a proxy.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
 

 

