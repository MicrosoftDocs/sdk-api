---
UID: NN:mswmdm.IMDSPDevice
title: IMDSPDevice (mswmdm.h)
description: The IMDSPDevice interface provides an instance-based association with a media device.
helpviewer_keywords: ["IMDSPDevice","IMDSPDevice interface [windows Media Device Manager]","IMDSPDevice interface [windows Media Device Manager]","described","IMDSPDeviceInterface","mswmdm/IMDSPDevice","wmdm.imdspdevice"]
old-location: wmdm\imdspdevice.htm
tech.root: WMDM
ms.assetid: 98f16547-4d8a-4422-ba08-c3c678142492
ms.date: 12/05/2018
ms.keywords: IMDSPDevice, IMDSPDevice interface [windows Media Device Manager], IMDSPDevice interface [windows Media Device Manager],described, IMDSPDeviceInterface, mswmdm/IMDSPDevice, wmdm.imdspdevice
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMDSPDevice
 - mswmdm/IMDSPDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDSPDevice
---

# IMDSPDevice interface


## -description

The <b>IMDSPDevice</b> interface provides an instance-based association with a media device. Using this interface, the client can get a storage media enumerator for the device, get information about the device, and send opaque (pass-through) commands to the device. <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2</a> extends <b>IMDSPDevice</b> by providing methods for getting video formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name. This interface is optional for the service provider but is recommended.

## -inheritance

The <b>IMDSPDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPDevice</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
