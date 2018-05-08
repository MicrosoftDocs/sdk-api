---
UID: NN:mbnapi.IMbnConnectionProfileManagerEvents
title: IMbnConnectionProfileManagerEvents
author: windows-driver-content
description: This notification interface signals an application about the arrival and removal of IMbnConnectionProfile interfaces in the system.
old-location: mbn\imbnconnectionprofilemanagerevents.htm
old-project: mbn
ms.assetid: 08ec0bff-898f-4a54-b711-ceae80e7329d
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnConnectionProfileManagerEvents, IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks], IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofilemanagerevents, mbnapi/IMbnConnectionProfileManagerEvents
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnConnectionProfileManagerEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfileManagerEvents interface


## -description


This notification interface signals an application about the arrival and removal of <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interfaces in the system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionProfileManagerEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionProfileManagerEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionProfileManagerEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94338c8c-2a89-412f-811e-5c50ecd9be70">OnConnectionProfileArrival</a>
</td>
<td align="left" width="63%">
A connection profile was added to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30b8c7fb-5a48-4025-aa94-18f17e7c8d19">OnConnectionProfileRemoval</a>
</td>
<td align="left" width="63%">
A connection profile was removed from the system.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionProfileManagerEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionProfileManagerEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



