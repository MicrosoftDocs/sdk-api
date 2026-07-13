---
UID: NN:mbnapi.IMbnDeviceServicesContext
title: IMbnDeviceServicesContext (mbnapi.h)
description: Allows for enumerating and retrieving Mobile Broadband device objects on the system.
helpviewer_keywords: ["IMbnDeviceServicesContext","IMbnDeviceServicesContext interface [Microsoft Broadband Networks]","IMbnDeviceServicesContext interface [Microsoft Broadband Networks]","described","mbn.imbndeviceservicescontext","mbnapi/IMbnDeviceServicesContext"]
old-location: mbn\imbndeviceservicescontext.htm
tech.root: mbn
ms.assetid: 0B97FCCD-0A90-4FA2-9122-B00BD3F1A033
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesContext, IMbnDeviceServicesContext interface [Microsoft Broadband Networks], IMbnDeviceServicesContext interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicescontext, mbnapi/IMbnDeviceServicesContext
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
 - IMbnDeviceServicesContext
 - mbnapi/IMbnDeviceServicesContext
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
 - IMbnDeviceServicesContext
---

# IMbnDeviceServicesContext interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Allows for enumerating and retrieving Mobile Broadband device objects on the system.

## -inheritance

The <b>IMbnDeviceServicesContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceServicesContext</b> also has these types of members:

## -remarks

<b>IMbnDeviceServicesContext</b> objects are provided by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesmanager-getdeviceservicescontext">GetDeviceServicesContext</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesmanager">IMbnDeviceServicesManager</a> interface.
