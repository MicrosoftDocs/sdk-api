---
UID: NN:mbnapi.IMbnConnectionContextEvents
title: IMbnConnectionContextEvents
author: windows-sdk-content
description: This notification interface is used to handle asynchronous provisioned context events.
old-location: mbn\imbnconnectioncontextevents.htm
tech.root: mbn
ms.assetid: 1f73260b-04db-410a-ade0-a835805b2b0a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMbnConnectionContextEvents, IMbnConnectionContextEvents interface [Microsoft Broadband Networks], IMbnConnectionContextEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectioncontextevents, mbnapi/IMbnConnectionContextEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionContextEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnConnectionContextEvents interface


## -description


This notification interface is used to handle asynchronous provisioned context events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionContextEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionContextEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionContextEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c8fa150-7c36-4ad8-ada8-2b17693671d9">OnProvisionedContextListChange</a>
</td>
<td align="left" width="63%">
A provisioned context is available or updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06e1071d-c541-4824-9b56-f2d18f41e972">OnSetProvisionedContextComplete</a>
</td>
<td align="left" width="63%">
The  provisioned context in the device has been set. 

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a>  object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionContextEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionContextEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



