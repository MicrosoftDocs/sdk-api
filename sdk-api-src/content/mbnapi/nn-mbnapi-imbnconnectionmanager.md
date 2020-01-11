---
UID: NN:mbnapi.IMbnConnectionManager
title: IMbnConnectionManager (mbnapi.h)
description: Provides access to IMbnConnection objects and connection notifications.
old-location: mbn\imbnconnectionmanager.htm
tech.root: mbn
ms.assetid: 20b9243d-1f20-4092-951a-fbacb2d55481
ms.date: 12/05/2018
ms.keywords: IMbnConnectionManager, IMbnConnectionManager interface [Microsoft Broadband Networks], IMbnConnectionManager interface [Microsoft Broadband Networks],described, mbn.imbnconnectionmanager, mbnapi/IMbnConnectionManager
f1_keywords:
- mbnapi/IMbnConnectionManager
dev_langs:
- c++
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
- IMbnConnectionManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionManager interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> objects and connection notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanager-getconnection">GetConnection</a>
</td>
<td align="left" width="63%">
Gets a specific connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanager-getconnections">GetConnections</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanagerevents">IMbnConnectionManagerEvents</a>
</td>
<td><b>IID_IMbnConnectionManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>
</td>
<td><b>IID_IMbnConnectionEvents</b></td>
</tr>
</table>
 



An application can obtain this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class id of <b>CLSID_IMbnConnectionManager</b>.

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



