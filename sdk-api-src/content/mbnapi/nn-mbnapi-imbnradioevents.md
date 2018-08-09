---
UID: NN:mbnapi.IMbnRadioEvents
title: IMbnRadioEvents
author: windows-sdk-content
description: Notification interface used to indicate a change in the radio state as well as the completion of a programatic change in the state .
old-location: mbn\imbnradioevents.htm
old-project: mbn
ms.assetid: f02fa823-c1ca-4867-981d-cb3107f7291b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnRadioEvents, IMbnRadioEvents interface [Microsoft Broadband Networks], IMbnRadioEvents interface [Microsoft Broadband Networks],described, mbn.imbnradioevents, mbnapi/IMbnRadioEvents
ms.prod: windows
ms.technology: windows-sdk
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
 - IMbnRadioEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRadioEvents interface


## -description


Notification interface used to indicate a change in the radio state as well as the completion of a programatic change in the state .


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRadioEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnRadioEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnRadioEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae7bf0d0-333b-429d-9dd1-9580745aad35">OnRadioStateChange</a>
</td>
<td align="left" width="63%">
The radio state of the device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e62ff68-0a6b-4e22-9cce-0df5da14fa6a">OnSetSoftwareRadioStateComplete</a>
</td>
<td align="left" width="63%">
A set software radio state operation has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a> interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnRadioEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnRadioEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



