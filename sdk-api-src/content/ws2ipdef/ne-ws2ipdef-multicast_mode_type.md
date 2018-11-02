---
UID: NE:ws2ipdef.MULTICAST_MODE_TYPE
title: MULTICAST_MODE_TYPE
author: windows-sdk-content
description: Specifies the filter mode for multicast group addresses.
old-location: winsock\multicast_mode_type.htm
tech.root: winsock
ms.assetid: 7ca9cb9b-618a-4e73-9e2a-18e55e5c00c0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MCAST_EXCLUDE, MCAST_INCLUDE, MULTICAST_MODE_TYPE, MULTICAST_MODE_TYPE enumeration [Winsock], winsock.multicast_mode_type, ws2ipdef/MCAST_EXCLUDE, ws2ipdef/MCAST_INCLUDE, ws2ipdef/MULTICAST_MODE_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ws2ipdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
api_name:
 - MULTICAST_MODE_TYPE
product: Windows
targetos: Windows
req.typenames: MULTICAST_MODE_TYPE
req.redist: 
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



This enumeration is supported on Windows Vistaand later.

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
 

 

