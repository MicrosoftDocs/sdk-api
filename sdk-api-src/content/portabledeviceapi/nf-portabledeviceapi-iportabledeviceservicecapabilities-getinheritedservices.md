---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPortableDeviceServiceCapabilities::GetInheritedServices


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
 

 

