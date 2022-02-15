---
UID: NN:mbnapi.IMbnDeviceServicesEvents
title: IMbnDeviceServicesEvents (mbnapi.h)
description: Signals an application about notification events related to Mobile Broadband device services on the system.
helpviewer_keywords: ["IMbnDeviceServicesEvents","IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","described","mbn.imbndeviceservicesevents","mbnapi/IMbnDeviceServicesEvents"]
old-location: mbn\imbndeviceservicesevents.htm
tech.root: mbn
ms.assetid: 66A388D0-C704-45D2-AD56-4F81E1928774
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents, IMbnDeviceServicesEvents interface [Microsoft Broadband Networks], IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicesevents, mbnapi/IMbnDeviceServicesEvents
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
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
 - IMbnDeviceServicesEvents
 - mbnapi/IMbnDeviceServicesEvents
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
 - IMbnDeviceServicesEvents
---

# IMbnDeviceServicesEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Signals an application about notification events related to Mobile Broadband device services on the system.

## -inheritance

The <b>IMbnDeviceServicesEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceServicesEvents</b> also has these types of members:

## -remarks

The following procedure describes how to register for notifications.<ol>
<li>Get an <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesmanager">IMbnDeviceServicesManager</a> object.</li>
<li>Call <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass IID_IMbnDeviceServicesEvents to RIID.</li>
<li>Call <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on an object that implements <b>IMbnDeviceServicesEvents</b> to PUNK.</li>
</ol>


Notifications can be terminated by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.


To view some code that registers for COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2001/january/msdn-magazine-january-2001">COM Connection Points article</a>.
