---
UID: NN:mbnapi.IMbnRegistrationEvents
title: IMbnRegistrationEvents (mbnapi.h)
author: windows-sdk-content
description: Notification interface used to indicate when registration events have occurred.
old-location: mbn\imbnregistrationevents.htm
tech.root: mbn
ms.assetid: f3b60a93-3b57-4c2c-9114-912ca47f16b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnRegistrationEvents, IMbnRegistrationEvents interface [Microsoft Broadband Networks], IMbnRegistrationEvents interface [Microsoft Broadband Networks],described, mbn.imbnregistrationevents, mbnapi/IMbnRegistrationEvents
ms.topic: interface
f1_keywords: 
 - "mbnapi/IMbnRegistrationEvents"
req.header: mbnapi.h
req.include-header: 
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
 - IMbnRegistrationEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnRegistrationEvents interface


## -description


Notification interface used to indicate when registration events have occurred.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRegistrationEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRegistrationEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onpacketservicestatechange">OnPacketServiceStateChange</a>
</td>
<td align="left" width="63%">
Indicates a change in the device packet service state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregistermodeavailable">OnRegisterModeAvailable</a>
</td>
<td align="left" width="63%">
Indicates that registration mode information is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onregisterstatechange">OnRegisterStateChange</a>
</td>
<td align="left" width="63%">
Indicates a change in the device's registration state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistrationevents-onsetregistermodecomplete">OnSetRegisterModeComplete</a>
</td>
<td align="left" width="63%">
Indicates that a set registration operation has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnRegistrationEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnRegistrationEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



