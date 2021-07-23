---
UID: NN:mbnapi.IMbnSignalEvents
title: IMbnSignalEvents (mbnapi.h)
description: Notification interface used to indicate that a signal event has occurred.
helpviewer_keywords: ["IMbnSignalEvents","IMbnSignalEvents interface [Microsoft Broadband Networks]","IMbnSignalEvents interface [Microsoft Broadband Networks]","described","mbn.imbnsignalevents","mbnapi/IMbnSignalEvents"]
old-location: mbn\imbnsignalevents.htm
tech.root: mbn
ms.assetid: 9e52168a-c6f9-4154-b8b9-8ae6cb771d46
ms.date: 12/05/2018
ms.keywords: IMbnSignalEvents, IMbnSignalEvents interface [Microsoft Broadband Networks], IMbnSignalEvents interface [Microsoft Broadband Networks],described, mbn.imbnsignalevents, mbnapi/IMbnSignalEvents
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
 - IMbnSignalEvents
 - mbnapi/IMbnSignalEvents
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
 - IMbnSignalEvents
---

# IMbnSignalEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification interface used to indicate that a signal event has occurred.

## -inheritance

The <b>IMbnSignalEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnSignalEvents</b> also has these types of members:

## -remarks

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>  interface by calling <b>QueryInterface</b> on an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnSignalEvents</b> to <i>riid</i>.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnSignalEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.
