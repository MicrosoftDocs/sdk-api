---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetInheritedServices
title: IPortableDeviceServiceCapabilities::GetInheritedServices
author: windows-sdk-content
description: Retrieves the services having the specified inheritance type.
old-location: wpdsdk\iportabledeviceservicecapabilities_getinheritedservices.htm
old-project: wpd_sdk
ms.assetid: f5640d6a-6c2f-4bd3-adff-628017f5b867
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetInheritedServices, GetInheritedServices method [Windows Portable Devices SDK], GetInheritedServices method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetInheritedServices method, IPortableDeviceServiceCapabilities.GetInheritedServices, IPortableDeviceServiceCapabilities::GetInheritedServices, portabledeviceapi/IPortableDeviceServiceCapabilities::GetInheritedServices, wpdsdk.iportabledeviceservicecapabilities_getinheritedservices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities.GetInheritedServices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceServiceCapabilities::GetInheritedServices


## -description


The  <b>GetInheritedServices</b> method retrieves the services having the  specified inheritance type.


## -parameters




### -param dwInheritanceType [in]

The type of inherited services to retrieve.


### -param ppServices [out]

The <a href="https://msdn.microsoft.com/41224958-a5a0-4e09-8733-d0ae036f68b9">IPortableDevicePropVariantCollection</a> interface that receives the list of services. If no inherited services are found, an empty collection is returned.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Currently, device services may only inherit by implementing an abstract service. This is analogous to how a class implements methods of an abstract interface or a virtual class in object-oriented programming. By implementing an abstract service, a device service will support all formats, properties, and method behavior that the abstract service describes. For instance, a  <b>Contacts</b> service may implement the <b>Anchor Sync</b> abstract service, where the device stores markers indicating which contacts were updated since the last synchronization with the PC. 

Possible values for the <i>dwInheritanceType</i> parameter are those defined in the <a href="https://msdn.microsoft.com/e7f5314a-75e8-4f36-8e18-d614eda7a097">WPD_SERVICE_INHERITANCE_TYPES</a> enumeration. (For Windows 7, only the <b>WPD_SERVICE_INHERITANCE_IMPLEMENTATION</b> enumeration constant is supported.)

If the value of the <i>dwInheritanceType</i> parameter is <b>WPD_SERVICE_INHERITANCE_IMPLEMENTATION</b>, each item in the collection specified by the <i>ppServices</i> parameter has variant type <b>VT_CLSID</b>.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

