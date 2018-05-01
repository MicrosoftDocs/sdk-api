---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetInheritedServices
title: IPortableDeviceServiceCapabilities::GetInheritedServices method
author: windows-driver-content
description: Retrieves the services having the specified inheritance type.
old-location: wpdsdk\iportabledeviceservicecapabilities_getinheritedservices.htm
old-project: wpd_sdk
ms.assetid: f5640d6a-6c2f-4bd3-adff-628017f5b867
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetInheritedServices method [Windows Portable Devices SDK], GetInheritedServices method [Windows Portable Devices SDK], IPortableDeviceServiceCapabilities interface, GetInheritedServices,IPortableDeviceServiceCapabilities.GetInheritedServices, IPortableDeviceServiceCapabilities, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK], GetInheritedServices method, IPortableDeviceServiceCapabilities::GetInheritedServices, portabledeviceapi/IPortableDeviceServiceCapabilities::GetInheritedServices, wpdsdk.iportabledeviceservicecapabilities_getinheritedservices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceServiceCapabilities.GetInheritedServices
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceServiceCapabilities::GetInheritedServices method


## -description


The  <b>GetInheritedServices</b> method retrieves the services having the  specified inheritance type.


## -parameters




### -param dwInheritanceType [in]

The type of inherited services to retrieve.


### -param ppServices [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that receives the list of services. If no inherited services are found, an empty collection is returned.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Currently, device services may only inherit by implementing an abstract service. This is analogous to how a class implements methods of an abstract interface or a virtual class in object-oriented programming. By implementing an abstract service, a device service will support all formats, properties, and method behavior that the abstract service describes. For instance, a  <b>Contacts</b> service may implement the <b>Anchor Sync</b> abstract service, where the device stores markers indicating which contacts were updated since the last synchronization with the PC. 

Possible values for the <i>dwInheritanceType</i> parameter are those defined in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597914">WPD_SERVICE_INHERITANCE_TYPES</a> enumeration. (For Windows 7, only the <b>WPD_SERVICE_INHERITANCE_IMPLEMENTATION</b> enumeration constant is supported.)

If the value of the <i>dwInheritanceType</i> parameter is <b>WPD_SERVICE_INHERITANCE_IMPLEMENTATION</b>, each item in the collection specified by the <i>ppServices</i> parameter has variant type <b>VT_CLSID</b>.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

