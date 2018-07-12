---
UID: NN:mbnapi.IMbnConnectionManager
title: IMbnConnectionManager
author: windows-sdk-content
description: Provides access to IMbnConnection objects and connection notifications.
old-location: mbn\imbnconnectionmanager.htm
old-project: mbn
ms.assetid: 20b9243d-1f20-4092-951a-fbacb2d55481
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMbnConnectionManager, IMbnConnectionManager interface [Microsoft Broadband Networks], IMbnConnectionManager interface [Microsoft Broadband Networks],described, mbn.imbnconnectionmanager, mbnapi/IMbnConnectionManager
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionManager interface


## -description


Provides access to <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> objects and connection notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnConnectionManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbeac057-77e3-438e-a7a9-b6f223a09dbe">GetConnection</a>
</td>
<td align="left" width="63%">
Gets a specific connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f4fd3b2-ed24-403a-ae5a-31821a2c7033">GetConnections</a>
</td>
<td align="left" width="63%">
Gets a list of all connections.

</td>
</tr>
</table> 


## -remarks



This interface can be used to access the following notification interfaces.<table>
<tr>
<th>Notification Sink to Register</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/153ab8c5-2b39-44a7-8c12-9f1df0012270">IMbnConnectionManagerEvents</a>
</td>
<td><b>IID_IMbnConnectionManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9135ba2e-62f6-495e-b136-9efc5f260581">IMbnConnectionEvents</a>
</td>
<td><b>IID_IMbnConnectionEvents</b></td>
</tr>
</table>
 



An application can obtain this interface by calling <a href="https://msdn.microsoft.com/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with a class id of <b>CLSID_IMbnConnectionManager</b>.

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="http://go.microsoft.com/fwlink/p/?linkid=109916">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <b>IMbnConnectionManager</b> object.</li>
<li>
For each notification sink to register, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109922">FindConnectionPoint</a> on the returned interface and pass IID corresponding to the notification sink to <i>riid</i>.

</li>
<li>For each connection point returned by step 2, call <a href="http://go.microsoft.com/fwlink/p/?linkid=109923">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements the matching notification interface to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=109924">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the "Client" section of the <a href="http://go.microsoft.com/fwlink/p/?linkid=109917">COM Connection Points</a> article.



