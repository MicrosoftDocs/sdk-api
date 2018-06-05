---
UID: NN:mbnapi.IMbnPinEvents
title: IMbnPinEvents
author: windows-sdk-content
description: This interface is a notification interface used to indicate when asynchronous PIN requests have completed.
old-location: mbn\imbnpinevents.htm
old-project: mbn
ms.assetid: 4bdaa4e5-880e-4d1f-aec1-36811a0f21c1
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IMbnPinEvents, IMbnPinEvents interface [Microsoft Broadband Networks], IMbnPinEvents interface [Microsoft Broadband Networks],described, mbn.imbnpinevents, mbnapi/IMbnPinEvents
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnPinEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnPinEvents interface


## -description


This interface is a notification interface used to indicate when asynchronous PIN requests have completed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPinEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnPinEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnPinEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0aa9944f-2a5c-4589-a109-bc0214b03d04">OnChangeComplete</a>
</td>
<td align="left" width="63%">
Indicates that a PIN change operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54fc0ec1-eb35-4403-b22a-4c50c4912604">OnDisableComplete</a>
</td>
<td align="left" width="63%">
Indicates that a PIN disable operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/577ba161-dbde-4541-8098-72ab682e548b">OnEnableComplete</a>
</td>
<td align="left" width="63%">
Indicates that a PIN enable operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a4bc731-e498-4afb-a648-0b49d2f592ca">OnEnterComplete</a>
</td>
<td align="left" width="63%">
Indicates that a PIN entry operation has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65a18fee-6d20-42fc-b1cb-ed0a440d76a5">OnUnblockComplete</a>
</td>
<td align="left" width="63%">
Indicates that a PIN unblock operation has completed.

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="https://msdn.microsoft.com/a998381e-47de-4352-bc84-b6edca2f3fcc">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnPinEvents</b> to <i>riid</i>.</li>
<li>Call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnPinEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



