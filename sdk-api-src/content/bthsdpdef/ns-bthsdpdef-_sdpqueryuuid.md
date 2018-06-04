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

# _SdpQueryUuid structure


## -description


The <b>SdpQueryUuid</b> structure facilitates searching for UUIDs.


## -struct-fields




### -field u

Union containing the UUID on which to search.


### -field u.switch_is

 


### -field u.switch_is.uuidType

 


### -field uuidType

Type of UUID being searched. Must be one of the three valid values from the SDP_SPECIFICTYPE enumeration:


<ul>
<li>SDP_ST_UUID16 - indicates u.uuid16 will be used in the search.</li>
<li>SDP_ST_UUID32 - indicates u.uuid32 will be used in the search.</li>
<li>SDP_ST_UUID128 - indicates u.uuid128 will be used in the search.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b208b7d6-305c-4acc-9c89-75721ff5dcb2">BTH_QUERY_SERVICE</a>
 

 

