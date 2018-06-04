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

# _IPX_ADDRESS_DATA structure


## -description



			The 
<b>IPX_ADDRESS_DATA</b> structure provides information about a specific adapter to which IPX is bound. Used in conjunction with 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> function calls that specify IPX_ADDRESS in the <i>optname</i> parameter.


## -struct-fields




### -field adapternum

0-based adapter number.


### -field netnum

IPX network number for the associated adapter.


### -field nodenum

IPX node address for the associated adapter.


### -field wan

Specifies whether the adapter is on a wide area network (WAN) link. When <b>TRUE</b>, the adapter is on a WAN link.


### -field status

Specifies whether the WAN link is up. <b>FALSE</b> indicates that the WAN link is up or the adapter is not on a WAN. Compare with the <b>wan</b> member to determine the meaning.


### -field maxpkt

Maximum allowable packet size, excluding the IPX header.


### -field linkspeed

Link speed, returned in 100 byte-per-second increments. For example, a 9600 byte-per-second link would return a value of 96.


## -remarks



Adapter numbers are base zero, so if there are eight adapters on a given computer, they are numbered 0-7. To determine the number of adapters present on the computer, call the 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> function with IPX_MAX_ADAPTER_NUM.




## -see-also




<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>
 

 

