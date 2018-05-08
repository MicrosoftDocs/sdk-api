---
UID: NN:mbnapi.IMbnRegistrationEvents
title: IMbnRegistrationEvents
author: windows-driver-content
description: Notification interface used to indicate when registration events have occurred.
old-location: mbn\imbnregistrationevents.htm
old-project: mbn
ms.assetid: f3b60a93-3b57-4c2c-9114-912ca47f16b2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnRegistrationEvents, IMbnRegistrationEvents interface [Microsoft Broadband Networks], IMbnRegistrationEvents interface [Microsoft Broadband Networks],described, mbn.imbnregistrationevents, mbnapi/IMbnRegistrationEvents
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnRegistrationEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRegistrationEvents interface


## -description


Notification interface used to indicate when registration events have occurred.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRegistrationEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnRegistrationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnRegistrationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19199009-a4ac-4bf9-adfc-46c06d861485">OnPacketServiceStateChange</a>
</td>
<td align="left" width="63%">
Indicates a change in the device packet service state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c916f16-e8f5-4c8a-942c-3a9ae11905a7">OnRegisterModeAvailable</a>
</td>
<td align="left" width="63%">
Indicates that registration mode information is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62393a9b-70e5-4819-8df1-59b94c1b6922">OnRegisterStateChange</a>
</td>
<td align="left" width="63%">
Indicates a change in the device's registration state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ca0776-bd1d-48a0-970a-39c8da69b394">OnSetRegisterModeComplete</a>
</td>
<td align="left" width="63%">
Indicates that a set registration operation has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnRegistrationEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnRegistrationEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



