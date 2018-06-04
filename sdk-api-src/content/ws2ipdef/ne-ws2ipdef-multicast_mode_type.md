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

# MULTICAST_MODE_TYPE enumeration


## -description


The <b>MULTICAST_MODE_TYPE</b> enumeration specifies the filter mode for multicast group addresses.


## -enum-fields




### -field MCAST_INCLUDE

The filter contains a list of IP addresses to include. 


### -field MCAST_EXCLUDE

The filter contains a list of IP addresses to exclude. 


## -remarks



This enumeration is supported on Windows Vista
  and later.

The <b>MULTICAST_MODE_TYPE</b> enumeration is used in the <b>gf_fmode</b> member of the <a href="https://msdn.microsoft.com/c8f442e0-e7c3-4421-a664-3f4e31a68eb9">GROUP_SOURCE_REQ</a> structure to determine if a list of IP addresses should included or excluded. The values from this enumeration can also be used in the <b>imsf_fmode</b> member of the <a href="https://msdn.microsoft.com/8d9d515e-9369-4d71-9614-6cbeb5557a5d">ip_msfilter</a> structure.

The <b>MULTICAST_MODE_TYPE</b> enumeration is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/053cf2c3-4f31-4f1e-be5c-d857e74d9465">GROUP_REQ</a>



<a href="https://msdn.microsoft.com/c8f442e0-e7c3-4421-a664-3f4e31a68eb9">GROUP_SOURCE_REQ</a>



<a href="https://msdn.microsoft.com/f729945b-b469-4baf-ac06-2431ee2d0e71">Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket Options</a>



<a href="https://msdn.microsoft.com/0bcf4c17-679d-42fc-b77e-722ce955d01f">ip_mreq</a>



<a href="https://msdn.microsoft.com/8d9d515e-9369-4d71-9614-6cbeb5557a5d">ip_msfilter</a>



<a href="https://msdn.microsoft.com/672ce465-357c-450c-83a2-3cbdb28e018c">ipv6_mreq</a>
 

 

