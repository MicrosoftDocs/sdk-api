---
UID: NN:portabledeviceapi.IPortableDevicePropertiesBulk
title: IPortableDevicePropertiesBulk (portabledeviceapi.h)
description: The IPortableDevicePropertiesBulk interface queries or sets multiple properties on multiple objects on a device, asynchronously.
helpviewer_keywords: ["IPortableDevicePropertiesBulk","IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK]","IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK]","described","IPortableDevicePropertiesBulkInterface","portabledeviceapi/IPortableDevicePropertiesBulk","wpdsdk.iportabledevicepropertiesbulk"]
old-location: wpdsdk\iportabledevicepropertiesbulk.htm
tech.root: wpdsdk
ms.assetid: 57cda40a-8573-4b6c-981e-770f35186038
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulk, IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK], IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],described, IPortableDevicePropertiesBulkInterface, portabledeviceapi/IPortableDevicePropertiesBulk, wpdsdk.iportabledevicepropertiesbulk
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDevicePropertiesBulk
 - portabledeviceapi/IPortableDevicePropertiesBulk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevicePropertiesBulk
---

# IPortableDevicePropertiesBulk interface


## -description

The <b>IPortableDevicePropertiesBulk</b> interface queries or sets multiple properties on multiple objects on a device, asynchronously. Information is returned by an application-implemented <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback</a> interface.

To get this interface, call <b>QueryInterface</b> on <b>IPortableDeviceProperties</b>. If the device does not support bulk operations, this call will fail with E_NOINTERFACE.

## -inheritance

The <b>IPortableDevicePropertiesBulk</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDevicePropertiesBulk</b> also has these types of members:

## -see-also

<a href="/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
