---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedEvents
title: IPortableDeviceServiceCapabilities::GetSupportedEvents (portabledeviceapi.h)
description: Retrieves the events supported by the service.
helpviewer_keywords: ["GetSupportedEvents","GetSupportedEvents method [Windows Portable Devices SDK]","GetSupportedEvents method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetSupportedEvents method","IPortableDeviceServiceCapabilities.GetSupportedEvents","IPortableDeviceServiceCapabilities::GetSupportedEvents","portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedEvents","wpdsdk.iportabledeviceservicecapabilities_getsupportedevents"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedevents.htm
tech.root: wpdsdk
ms.assetid: 19621abc-34df-4c16-8cb7-f0d9d7fb7e06
ms.date: 12/05/2018
ms.keywords: GetSupportedEvents, GetSupportedEvents method [Windows Portable Devices SDK], GetSupportedEvents method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedEvents method, IPortableDeviceServiceCapabilities.GetSupportedEvents, IPortableDeviceServiceCapabilities::GetSupportedEvents, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedEvents, wpdsdk.iportabledeviceservicecapabilities_getsupportedevents
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
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
 - IPortableDeviceServiceCapabilities::GetSupportedEvents
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities.GetSupportedEvents
---

# IPortableDeviceServiceCapabilities::GetSupportedEvents


## -description

The <b>GetSupportedEvents</b> method retrieves the events supported by the service.

## -parameters

### -param ppEvents [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that receives the list of events.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>