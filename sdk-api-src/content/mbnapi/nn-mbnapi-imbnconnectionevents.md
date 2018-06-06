---
UID: NN:mbnapi.IMbnConnectionEvents
title: IMbnConnectionEvents
author: windows-sdk-content
description: This notification interface signals an application about change and completion status of asynchronous connection requests.
old-location: mbn\imbnconnectionevents.htm
old-project: mbn
ms.assetid: 9135ba2e-62f6-495e-b136-9efc5f260581
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnConnectionEvents, IMbnConnectionEvents interface [Microsoft Broadband Networks], IMbnConnectionEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectionevents, mbnapi/IMbnConnectionEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionEvents interface


## -description


This notification interface signals an application about change and completion status of asynchronous connection requests.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d770eda5-43f4-44d3-a870-fc54f9374610">OnConnectComplete</a>
</td>
<td align="left" width="63%">
A connection operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5392e5b7-eac7-40f1-b5cd-adde5a6ff1b8">OnConnectStateChange</a>
</td>
<td align="left" width="63%">
The connection state of the device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d225823-2b9b-4c3a-b847-7b2b9a13d121">OnDisconnectComplete</a>
</td>
<td align="left" width="63%">
A disconnect operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4f243b0-e6d5-4afc-85ad-0f88140c3beb">OnVoiceCallStateChange</a>
</td>
<td align="left" width="63%">
The voice call state has changed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/20b9243d-1f20-4092-951a-fbacb2d55481">IMbnConnectionManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



