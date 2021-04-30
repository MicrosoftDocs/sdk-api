---
UID: NN:mbnapi.IMbnConnectionManagerEvents
title: IMbnConnectionManagerEvents (mbnapi.h)
description: This notification interface signals an application about the arrival and removal of IMbnConnection interfaces in the system.
helpviewer_keywords: ["IMbnConnectionManagerEvents","IMbnConnectionManagerEvents interface [Microsoft Broadband Networks]","IMbnConnectionManagerEvents interface [Microsoft Broadband Networks]","described","mbn.imbnconnectionmanagerevents","mbnapi/IMbnConnectionManagerEvents"]
old-location: mbn\imbnconnectionmanagerevents.htm
tech.root: mbn
ms.assetid: 153ab8c5-2b39-44a7-8c12-9f1df0012270
ms.date: 12/05/2018
ms.keywords: IMbnConnectionManagerEvents, IMbnConnectionManagerEvents interface [Microsoft Broadband Networks], IMbnConnectionManagerEvents interface [Microsoft Broadband Networks],described, mbn.imbnconnectionmanagerevents, mbnapi/IMbnConnectionManagerEvents
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
 - IMbnConnectionManagerEvents
 - mbnapi/IMbnConnectionManagerEvents
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
 - IMbnConnectionManagerEvents
---

# IMbnConnectionManagerEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification interface signals an application about the arrival and removal of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interfaces in the system.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionManagerEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionManagerEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanager">IMbnConnectionManager</a> object.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnConnectionManagerEvents</b> to <i>riid</i>.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnConnectionManagerEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.
