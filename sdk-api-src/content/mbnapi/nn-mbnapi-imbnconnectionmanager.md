---
UID: NN:mbnapi.IMbnConnectionManager
title: IMbnConnectionManager (mbnapi.h)
description: Provides access to IMbnConnection objects and connection notifications.
helpviewer_keywords: ["IMbnConnectionManager","IMbnConnectionManager interface [Microsoft Broadband Networks]","IMbnConnectionManager interface [Microsoft Broadband Networks]","described","mbn.imbnconnectionmanager","mbnapi/IMbnConnectionManager"]
old-location: mbn\imbnconnectionmanager.htm
tech.root: mbn
ms.assetid: 20b9243d-1f20-4092-951a-fbacb2d55481
ms.date: 12/05/2018
ms.keywords: IMbnConnectionManager, IMbnConnectionManager interface [Microsoft Broadband Networks], IMbnConnectionManager interface [Microsoft Broadband Networks],described, mbn.imbnconnectionmanager, mbnapi/IMbnConnectionManager
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnConnectionManager
 - mbnapi/IMbnConnectionManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionManager
---

# IMbnConnectionManager interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> objects and connection notifications.

## -inheritance

The <b>IMbnConnectionManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionManager</b> also has these types of members:

## -remarks

This interface can be used to access the following notification interfaces.<table>
<tr>
<th>Notification Sink to Register</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanagerevents">IMbnConnectionManagerEvents</a>
</td>
<td><b>IID_IMbnConnectionManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>
</td>
<td><b>IID_IMbnConnectionEvents</b></td>
</tr>
</table>
 



An application can obtain this interface by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class id of <b>CLSID_IMbnConnectionManager</b>.

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <b>IMbnConnectionManager</b> object.</li>
<li>
For each notification sink to register, call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass IID corresponding to the notification sink to <i>riid</i>.

</li>
<li>For each connection point returned by step 2, call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements the matching notification interface to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the "Client" section of the <a href="/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.
