---
UID: NN:portabledeviceapi.IPortableDevice
title: IPortableDevice (portabledeviceapi.h)
description: The IPortableDevice interface provides access to a portable device.
helpviewer_keywords: ["IPortableDevice","IPortableDevice interface [Windows Portable Devices SDK]","IPortableDevice interface [Windows Portable Devices SDK]","described","IPortableDeviceInterface","portabledeviceapi/IPortableDevice","wpdsdk.iportabledevice"]
old-location: wpdsdk\iportabledevice.htm
tech.root: wpdsdk
ms.assetid: 98c48e56-56b8-4800-b52b-ac08f2abf27e
ms.date: 12/05/2018
ms.keywords: IPortableDevice, IPortableDevice interface [Windows Portable Devices SDK], IPortableDevice interface [Windows Portable Devices SDK],described, IPortableDeviceInterface, portabledeviceapi/IPortableDevice, wpdsdk.iportabledevice
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
 - IPortableDevice
 - portabledeviceapi/IPortableDevice
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
 - IPortableDevice
---

# IPortableDevice interface


## -description

The <b>IPortableDevice</b> interface provides access to a portable device.

To create and open this interface, first call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with <b>CLSID_PortableDeviceFTM</b>  or <b>CLSID_PortableDevice</b> to retrieve an <b>IPortableDevice</b> interface, and then call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-open">Open</a> to open a connection to the device.

## -inheritance

The <b>IPortableDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDevice</b> also has these types of members:

## -remarks

The client interfaces are designed to be used for any WPD object; it is not necessary to create a new instance for each object referenced by the application. After an application opens an instance of the <b>IPortableDevice</b> interface, it should open and cache any other WPD client interfaces that it will require.
      

For Windows 7, <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDevice</a> supports two CLSIDs for <b>CoCreateInstance</b>. <b>CLSID_PortableDevice</b> returns an <b>IPortableDevice</b> pointer that does not aggregate the free-threaded marshaler; <b>CLSID_PortableDeviceFTM</b> is a new CLSID that returns an <b>IPortableDevice</b> pointer that aggregates the free-threaded marshaler.  Both pointers support the same functionality otherwise.

Applications that live in Single Threaded Apartments should use <b>CLSID_PortableDeviceFTM</b> as this eliminates the overhead of interface pointer marshaling.  <b>CLSID_PortableDevice</b> is still supported for legacy applications.

## -see-also

<a href="/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
