---
UID: NN:portabledeviceapi.IPortableDeviceProperties
title: IPortableDeviceProperties (portabledeviceapi.h)
description: The IPortableDeviceProperties interface retrieves, adds, or deletes properties from an object on a device, or the device itself.
helpviewer_keywords: ["IPortableDeviceProperties","IPortableDeviceProperties interface [Windows Portable Devices SDK]","IPortableDeviceProperties interface [Windows Portable Devices SDK]","described","IPortableDevicePropertiesInterface","portabledeviceapi/IPortableDeviceProperties","wpdsdk.iportabledeviceproperties"]
old-location: wpdsdk\iportabledeviceproperties.htm
tech.root: wpdsdk
ms.assetid: 4555e85b-c667-466c-a527-cc29ca7a6aee
ms.date: 12/05/2018
ms.keywords: IPortableDeviceProperties, IPortableDeviceProperties interface [Windows Portable Devices SDK], IPortableDeviceProperties interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesInterface, portabledeviceapi/IPortableDeviceProperties, wpdsdk.iportabledeviceproperties
req.header: portabledeviceapi.h
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
 - IPortableDeviceProperties
 - portabledeviceapi/IPortableDeviceProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - portabledeviceapi.h
api_name:
 - IPortableDeviceProperties
---

# IPortableDeviceProperties interface


## -description

The <b>IPortableDeviceProperties</b> interface retrieves, adds, or deletes properties from an object on a device, or the device itself. To get this interface, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-properties">IPortableDeviceContent::Properties</a> on an object. To get this interface for the object, specify <b>WPD_DEVICE_OBJECT_ID</b> in <b>GetValues</b>.

## -inheritance

The <b>IPortableDeviceProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceProperties</b> also has these types of members:

## -see-also

<a href="/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
