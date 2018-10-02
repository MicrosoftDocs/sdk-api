---
UID: NN:mbnapi.IMbnInterfaceManagerEvents
title: IMbnInterfaceManagerEvents
author: windows-sdk-content
description: This notification interface signals an application about the arrival and removal of devices in the system.
old-location: mbn\imbninterfacemanagerevents.htm
tech.root: mbn
ms.assetid: 1d421668-cbea-4457-bbc3-dad1b53a5d70
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMbnInterfaceManagerEvents, IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks], IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks],described, mbn.imbninterfacemanagerevents, mbnapi/IMbnInterfaceManagerEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMbnInterfaceManagerEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnInterfaceManagerEvents interface


## -description


This notification interface signals an application about the arrival and removal of devices in the system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnInterfaceManagerEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnInterfaceManagerEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnInterfaceManagerEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a65aed6-34d4-420b-b175-a2a778712771">OnInterfaceArrival</a>
</td>
<td align="left" width="63%">
A new device was added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7c96d35-20e1-46e2-82db-4b1fc03cdd22">OnInterfaceRemoval</a>
</td>
<td align="left" width="63%">
A device was removed from the system.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnInterfaceManagerEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnInterfaceManagerEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



