---
UID: NN:mbnapi.IMbnConnectionProfileManagerEvents
title: IMbnConnectionProfileManagerEvents (mbnapi.h)
description: This notification interface signals an application about the arrival and removal of IMbnConnectionProfile interfaces in the system.
helpviewer_keywords: ["IMbnConnectionProfileManagerEvents","IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks]","IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks]","described","mbn.imbnconnectionprofilemanagerevents","mbnapi/IMbnConnectionProfileManagerEvents"]
old-location: mbn\imbnconnectionprofilemanagerevents.htm
tech.root: mbn
ms.assetid: 08ec0bff-898f-4a54-b711-ceae80e7329d
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileManagerEvents, IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks], IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofilemanagerevents, mbnapi/IMbnConnectionProfileManagerEvents
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
 - IMbnConnectionProfileManagerEvents
 - mbnapi/IMbnConnectionProfileManagerEvents
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
 - IMbnConnectionProfileManagerEvents
---

# IMbnConnectionProfileManagerEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification interface signals an application about the arrival and removal of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interfaces in the system.

## -inheritance

The <b>IMbnConnectionProfileManagerEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionProfileManagerEvents</b> also has these types of members:

## -remarks

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a> object.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionProfileManagerEvents</b> to <i>riid</i>.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionProfileManagerEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.
