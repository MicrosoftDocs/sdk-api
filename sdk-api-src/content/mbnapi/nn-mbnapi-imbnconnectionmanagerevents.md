---
UID: NN:mbnapi.IMbnConnectionManagerEvents
title: IMbnConnectionManagerEvents
author: windows-driver-content
description: This notification interface signals an application about the arrival and removal of IMbnConnection interfaces in the system.
old-location: mbn\imbnconnectionmanagerevents.htm
old-project: mbn
ms.assetid: 153ab8c5-2b39-44a7-8c12-9f1df0012270
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnConnectionManagerEvents, IMbnConnectionManagerEvents interface [Microsoft Broadband Networks], IMbnConnectionManagerEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectionmanagerevents, mbnapi/IMbnConnectionManagerEvents
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
-	IMbnConnectionManagerEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionManagerEvents interface


## -description


This notification interface signals an application about the arrival and removal of <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> interfaces in the system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionManagerEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionManagerEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionManagerEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88e48ce0-b2eb-431e-be0f-03b1d22ca61b">OnConnectionArrival</a>
</td>
<td align="left" width="63%">
A new connection was added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/020ee1ad-cab5-4a27-b97b-160319d84ac8">OnConnectionRemoval</a>
</td>
<td align="left" width="63%">
A connection was removed from the system.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/20b9243d-1f20-4092-951a-fbacb2d55481">IMbnConnectionManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionManagerEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionManagerEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



