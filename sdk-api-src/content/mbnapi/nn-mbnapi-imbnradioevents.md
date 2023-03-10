---
UID: NN:mbnapi.IMbnRadioEvents
title: IMbnRadioEvents (mbnapi.h)
description: Notification interface used to indicate a change in the radio state as well as the completion of a programmatic change in the state .
helpviewer_keywords: ["IMbnRadioEvents","IMbnRadioEvents interface [Microsoft Broadband Networks]","IMbnRadioEvents interface [Microsoft Broadband Networks]","described","mbn.imbnradioevents","mbnapi/IMbnRadioEvents"]
old-location: mbn\imbnradioevents.htm
tech.root: mbn
ms.assetid: f02fa823-c1ca-4867-981d-cb3107f7291b
ms.date: 12/05/2018
ms.keywords: IMbnRadioEvents, IMbnRadioEvents interface [Microsoft Broadband Networks], IMbnRadioEvents interface [Microsoft Broadband Networks],described, mbn.imbnradioevents, mbnapi/IMbnRadioEvents
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
 - IMbnRadioEvents
 - mbnapi/IMbnRadioEvents
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
 - IMbnRadioEvents
---

# IMbnRadioEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification interface used to indicate a change in the radio state as well as the completion of a programmatic change in the state .

## -inheritance

The <b>IMbnRadioEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRadioEvents</b> also has these types of members:

## -remarks

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> interface by calling <b>QueryInterface</b> on an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnRadioEvents</b> to <i>riid</i>.</li>
<li>Call <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnRadioEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.
