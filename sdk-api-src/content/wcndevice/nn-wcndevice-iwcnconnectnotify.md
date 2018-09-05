---
UID: NN:wcndevice.IWCNConnectNotify
title: IWCNConnectNotify
author: windows-sdk-content
description: Use this interface to receive a success or failure notification when a Windows Connect Now connect session completes.
old-location: wcn\iwcnconnectnotify.htm
old-project: wcn
ms.assetid: 63ea2b5a-4bec-4050-9a61-962a1faef0a0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWCNConnectNotify, IWCNConnectNotify interface [Windows Connect Now], IWCNConnectNotify interface [Windows Connect Now],described, wcn.iwcnconnectnotify, wcndevice/IWCNConnectNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wcndevice.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WCN_SESSION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNConnectNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWCNConnectNotify interface


## -description


Use this interface to receive a success or failure notification when a Windows Connect Now connect session completes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCNConnectNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWCNConnectNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWCNConnectNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdf0394a-f5e6-49cf-bd18-9c3c2b689e50">ConnectFailed</a>
</td>
<td align="left" width="63%">
A callback method that indicates a <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a> operation failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79c8482a-5cb2-44a7-b324-964bfedd3d2f">ConnectSucceeded</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/79c8482a-5cb2-44a7-b324-964bfedd3d2f">IWCNConnectNotify::ConnectSucceeded</a> callback method that indicates a successful <a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice::Connect</a> operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6">IWCNDevice:Connect</a>
 

 

