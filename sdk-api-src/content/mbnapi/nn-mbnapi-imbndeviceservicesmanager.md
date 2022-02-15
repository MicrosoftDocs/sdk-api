---
UID: NN:mbnapi.IMbnDeviceServicesManager
title: IMbnDeviceServicesManager (mbnapi.h)
description: Provides access to IMbnDeviceServicesContext objects and Mobile Broadband device service notifications.
helpviewer_keywords: ["IMbnDeviceServicesManager","IMbnDeviceServicesManager interface [Microsoft Broadband Networks]","IMbnDeviceServicesManager interface [Microsoft Broadband Networks]","described","mbn.imbndeviceservicesmanager","mbnapi/IMbnDeviceServicesManager"]
old-location: mbn\imbndeviceservicesmanager.htm
tech.root: mbn
ms.assetid: 6CFF2275-0649-4009-84F2-0657B2FF281C
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesManager, IMbnDeviceServicesManager interface [Microsoft Broadband Networks], IMbnDeviceServicesManager interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicesmanager, mbnapi/IMbnDeviceServicesManager
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
 - IMbnDeviceServicesManager
 - mbnapi/IMbnDeviceServicesManager
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
 - IMbnDeviceServicesManager
---

# IMbnDeviceServicesManager interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> objects and Mobile Broadband device service notifications.

## -inheritance

The <b>IMbnDeviceServicesManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceServicesManager</b> also has these types of members:

## -remarks

The following procedure describes how to register for notifications.<ol>
<li>Get an <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an <b>IMbnDeviceServicesManager</b> object.</li>
<li>Call <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass IID_IMbnDeviceServicesEvents to RIID.</li>
<li>Call <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on an object that implements <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> to PUNK.</li>
</ol>


Notifications can be terminated by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.


For sample code that registers COM notifications, see the Client section of the <a href="/archive/msdn-magazine/2001/january/msdn-magazine-january-2001">COM Connection Points article</a>.
