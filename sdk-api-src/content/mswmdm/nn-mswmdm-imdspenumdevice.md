---
UID: NN:mswmdm.IMDSPEnumDevice
title: IMDSPEnumDevice (mswmdm.h)
description: The IMDSPEnumDevice interface is used to enumerate the media devices.
helpviewer_keywords: ["IMDSPEnumDevice","IMDSPEnumDevice interface [windows Media Device Manager]","IMDSPEnumDevice interface [windows Media Device Manager]","described","IMDSPEnumDeviceInterface","mswmdm/IMDSPEnumDevice","wmdm.imdspenumdevice"]
old-location: wmdm\imdspenumdevice.htm
tech.root: WMDM
ms.assetid: 9a296937-6f8b-4f04-989f-3a5d4c6f7b85
ms.date: 12/05/2018
ms.keywords: IMDSPEnumDevice, IMDSPEnumDevice interface [windows Media Device Manager], IMDSPEnumDevice interface [windows Media Device Manager],described, IMDSPEnumDeviceInterface, mswmdm/IMDSPEnumDevice, wmdm.imdspenumdevice
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
 - IMDSPEnumDevice
 - mswmdm/IMDSPEnumDevice
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
 - IMDSPEnumDevice
---

# IMDSPEnumDevice interface


## -description

The <b>IMDSPEnumDevice</b> interface is used to enumerate the media devices. For more information on enumeration, see the Microsoft COM documentation on the COM page at the <a href="/windows/win32/com/the-component-object-model">Microsoft Web site</a>. The <b>IMDSPEnumDevice</b> interface is implemented on the device enumerator object. The only valid way to create a device enumerator object is to call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices">IMDServiceProvider::EnumDevices</a>. If the device implements <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice">IMDServiceProvider2::CreateDevice</a>, this enumerator should enumerate only non-Plug and Play devices. The device enumerator should enumerate only the devices that are attached to the computer and are supported by the service provider.

## -inheritance

The <b>IMDSPEnumDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPEnumDevice</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices">IMDServiceProvider::EnumDevices</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
