---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetInheritedServices
title: IPortableDeviceServiceCapabilities::GetInheritedServices (portabledeviceapi.h)
description: Retrieves the services having the specified inheritance type.
helpviewer_keywords: ["GetInheritedServices","GetInheritedServices method [Windows Portable Devices SDK]","GetInheritedServices method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","GetInheritedServices method","IPortableDeviceServiceCapabilities.GetInheritedServices","IPortableDeviceServiceCapabilities::GetInheritedServices","portabledeviceapi/IPortableDeviceServiceCapabilities::GetInheritedServices","wpdsdk.iportabledeviceservicecapabilities_getinheritedservices"]
old-location: wpdsdk\iportabledeviceservicecapabilities_getinheritedservices.htm
tech.root: wpdsdk
ms.assetid: f5640d6a-6c2f-4bd3-adff-628017f5b867
ms.date: 12/05/2018
ms.keywords: GetInheritedServices, GetInheritedServices method [Windows Portable Devices SDK], GetInheritedServices method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetInheritedServices method, IPortableDeviceServiceCapabilities.GetInheritedServices, IPortableDeviceServiceCapabilities::GetInheritedServices, portabledeviceapi/IPortableDeviceServiceCapabilities::GetInheritedServices, wpdsdk.iportabledeviceservicecapabilities_getinheritedservices
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
 - IPortableDeviceServiceCapabilities::GetInheritedServices
 - portabledeviceapi/IPortableDeviceServiceCapabilities::GetInheritedServices
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
 - IPortableDeviceServiceCapabilities.GetInheritedServices
---

# IPortableDeviceServiceCapabilities::GetInheritedServices


## -description

The  <b>GetInheritedServices</b> method retrieves the services having the  specified inheritance type.

## -parameters

### -param dwInheritanceType [in]

The type of inherited services to retrieve.

### -param ppServices [out]

The <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that receives the list of services. If no inherited services are found, an empty collection is returned.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

Currently, device services may only inherit by implementing an abstract service. This is analogous to how a class implements methods of an abstract interface or a virtual class in object-oriented programming. By implementing an abstract service, a device service will support all formats, properties, and method behavior that the abstract service describes. For instance, a  <b>Contacts</b> service may implement the <b>Anchor Sync</b> abstract service, where the device stores markers indicating which contacts were updated since the last synchronization with the PC. 

Possible values for the <i>dwInheritanceType</i> parameter are those defined in the <a href="/windows/desktop/wpd_sdk/wpd-service-inheritance-types2">WPD_SERVICE_INHERITANCE_TYPES</a> enumeration. (For Windows 7, only the <b>WPD_SERVICE_INHERITANCE_IMPLEMENTATION</b> enumeration constant is supported.)

If the value of the <i>dwInheritanceType</i> parameter is <b>WPD_SERVICE_INHERITANCE_IMPLEMENTATION</b>, each item in the collection specified by the <i>ppServices</i> parameter has variant type <b>VT_CLSID</b>.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>