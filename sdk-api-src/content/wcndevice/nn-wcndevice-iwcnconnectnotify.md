---
UID: NN:wcndevice.IWCNConnectNotify
title: IWCNConnectNotify (wcndevice.h)
description: Use this interface to receive a success or failure notification when a Windows Connect Now connect session completes.
helpviewer_keywords: ["IWCNConnectNotify","IWCNConnectNotify interface [Windows Connect Now]","IWCNConnectNotify interface [Windows Connect Now]","described","wcn.iwcnconnectnotify","wcndevice/IWCNConnectNotify"]
old-location: wcn\iwcnconnectnotify.htm
tech.root: wcn
ms.assetid: 63ea2b5a-4bec-4050-9a61-962a1faef0a0
ms.date: 12/05/2018
ms.keywords: IWCNConnectNotify, IWCNConnectNotify interface [Windows Connect Now], IWCNConnectNotify interface [Windows Connect Now],described, wcn.iwcnconnectnotify, wcndevice/IWCNConnectNotify
req.header: wcndevice.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWCNConnectNotify
 - wcndevice/IWCNConnectNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNConnectNotify
---

# IWCNConnectNotify interface


## -description

Use this interface to receive a success or failure notification when a Windows Connect Now connect session completes.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCNConnectNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWCNConnectNotify</b> also has these types of members:
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
<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcnconnectnotify-connectfailed">ConnectFailed</a>
</td>
<td align="left" width="63%">
A callback method that indicates a <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> operation failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcnconnectnotify-connectsucceeded">ConnectSucceeded</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcnconnectnotify-connectsucceeded">IWCNConnectNotify::ConnectSucceeded</a> callback method that indicates a successful <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice:Connect</a>