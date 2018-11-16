---
UID: NN:mbnapi.IMbnVendorSpecificEvents
title: IMbnVendorSpecificEvents
author: windows-sdk-content
description: This notification interface signals an application of the completion status of vendor-specific operations and other vendor-specific changes in the device state.
old-location: mbn\imbnvendorspecificevents.htm
tech.root: mbn
ms.assetid: 28507e68-5eaa-4b9d-bbb4-e276f4c213d5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMbnVendorSpecificEvents, IMbnVendorSpecificEvents interface [Microsoft Broadband Networks], IMbnVendorSpecificEvents interface [Microsoft Broadband Networks],described, mbn.imbnvendorspecificevents, mbnapi/IMbnVendorSpecificEvents
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
 - IMbnVendorSpecificEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnVendorSpecificEvents interface


## -description


This notification interface signals an application of the completion status of vendor-specific operations and other vendor-specific changes in the device state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnVendorSpecificEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnVendorSpecificEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnVendorSpecificEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3d10e9c-b60f-42e8-adaa-2c0ba3c77718">OnEventNotification</a>
</td>
<td align="left" width="63%">
A event has occurred in the miniport driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc45b203-3e8e-436c-a554-164634026ecc">OnSetVendorSpecificComplete</a>
</td>
<td align="left" width="63%">
A vendor-specific operation call has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnVendorSpecificEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnVendorSpecificEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



