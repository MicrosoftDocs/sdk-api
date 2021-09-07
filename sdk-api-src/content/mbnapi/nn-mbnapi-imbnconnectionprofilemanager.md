---
UID: NN:mbnapi.IMbnConnectionProfileManager
title: IMbnConnectionProfileManager (mbnapi.h)
description: Provides access to connection profiles and connection notifications.
helpviewer_keywords: ["IMbnConnectionProfileManager","IMbnConnectionProfileManager interface [Microsoft Broadband Networks]","IMbnConnectionProfileManager interface [Microsoft Broadband Networks]","described","mbn.imbnconnectionprofilemanager","mbnapi/IMbnConnectionProfileManager"]
old-location: mbn\imbnconnectionprofilemanager.htm
tech.root: mbn
ms.assetid: a55e4183-f914-4064-a391-3bd31ca59160
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileManager, IMbnConnectionProfileManager interface [Microsoft Broadband Networks], IMbnConnectionProfileManager interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofilemanager, mbnapi/IMbnConnectionProfileManager
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnConnectionProfileManager
 - mbnapi/IMbnConnectionProfileManager
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
 - IMbnConnectionProfileManager
---

# IMbnConnectionProfileManager interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to connection profiles and connection notifications.

## -inheritance

The <b>IMbnConnectionProfileManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionProfileManager</b> also has these types of members:

## -remarks

This interface can be used to access the following notification interfaces.<table>
<tr>
<th>Notification Sink to Register   </th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a>
</td>
<td><b>IID_IMbnConnectionProfileManagerEvents</b></td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofileevents">MbnConnectionProfileEvents</a>
</td>
<td><b>IID_IMbnConnectionProfileEvents</b></td>
</tr>
</table>
 



An application can obtain this interface by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class id of <b>CLSID_IMbnConnectionProfileManager</b>.

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <b>IMbnConnectionProfileManager</b> object.</li>
<li>
For each notification sink to register, call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass IID corresponding to the notification sink to <i>riid</i>.

</li>
<li>For each connection point returned by step 2, call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements the matching notification interface to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.
