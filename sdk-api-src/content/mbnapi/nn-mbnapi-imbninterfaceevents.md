---
UID: NN:mbnapi.IMbnInterfaceEvents
title: IMbnInterfaceEvents
author: windows-sdk-content
description: This interface is a notification interface used to handle asynchronous IMbnInterface method calls as well as changes in the device state.
old-location: mbn\imbninterfaceevents.htm
old-project: mbn
ms.assetid: 3c641f14-9f53-4d69-9faa-2491189083df
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnInterfaceEvents, IMbnInterfaceEvents interface [Microsoft Broadband Networks], IMbnInterfaceEvents interface [Microsoft Broadband Networks],described, mbn.imbninterfaceevents, mbnapi/IMbnInterfaceEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnInterfaceEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterfaceEvents interface


## -description


This interface is a notification interface used to handle asynchronous <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> method calls as well as changes in the device state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterfaceEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnInterfaceEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnInterfaceEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/637e0f6b-102f-436c-b0ec-edef16245675">OnEmergencyModeChange</a>
</td>
<td align="left" width="63%">
The emergency mode has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4da50033-d55c-4878-b05c-cbc43c156da0">OnHomeProviderAvailable</a>
</td>
<td align="left" width="63%">
Home provider information is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeeffe13-307b-45f3-aa24-c33c621aa18e">OnInterfaceCapabilityAvailable</a>
</td>
<td align="left" width="63%">
Device capability information is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccede3de-4dfd-469f-afb4-d1424c56c7bc">OnPreferredProvidersChange</a>
</td>
<td align="left" width="63%">
The list of preferred providers has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb4364b8-cbbf-44c7-ae13-66950ce614e9">OnReadyStateChange</a>
</td>
<td align="left" width="63%">
The ready state has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6320c76b-b8a6-44dc-88bb-e20a85d5cfca">OnScanNetworkComplete</a>
</td>
<td align="left" width="63%">
An operation to scan the network has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cd5d185-ff0f-45f4-91fc-da601d256914">OnSetPreferredProvidersComplete</a>
</td>
<td align="left" width="63%">
An operation to change the preferred provider completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26d4fbdb-9c13-4934-a6bb-df581d0c18e9">OnSubscriberInformationChange</a>
</td>
<td align="left" width="63%">
The subscriber information has changed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnInterfaceEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnInterfaceEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



