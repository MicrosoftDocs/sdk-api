---
UID: NN:mbnapi.IMbnDeviceService
title: IMbnDeviceService (mbnapi.h)
description: Allows for communicating with a device service on a particular Mobile Broadband device.
helpviewer_keywords: ["IMbnDeviceService","IMbnDeviceService interface [Microsoft Broadband Networks]","IMbnDeviceService interface [Microsoft Broadband Networks]","described","mbn.imbndeviceservice","mbnapi/IMbnDeviceService"]
old-location: mbn\imbndeviceservice.htm
tech.root: mbn
ms.assetid: 5C587408-DF03-4123-BA5A-C2CCC378F60A
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService, IMbnDeviceService interface [Microsoft Broadband Networks], IMbnDeviceService interface [Microsoft Broadband Networks],described, mbn.imbndeviceservice, mbnapi/IMbnDeviceService
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
 - IMbnDeviceService
 - mbnapi/IMbnDeviceService
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
 - IMbnDeviceService
---

# IMbnDeviceService interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Allows for communicating with a device service on a particular Mobile Broadband device.

## -inheritance

The <b>IMbnDeviceService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceService</b> also has these types of members:

## -remarks

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> objects are provided by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-getdeviceservice">GetDeviceService</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> interface.
