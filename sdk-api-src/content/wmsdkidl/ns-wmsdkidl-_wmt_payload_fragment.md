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

# _WMT_PAYLOAD_FRAGMENT structure


## -description



The <b>WMT_PAYLOAD_FRAGMENT</b> structure contains the information needed to extract a payload fragment from a buffer and identifies the payload to which the fragment belongs. An array of <b>WMT_PAYLOAD_FRAGMENT</b> structures is used as a member of the <b>WMT_FILESINK_DATA_UNIT</b> structure to provide access to each payload fragment in a packet.




## -struct-fields




### -field dwPayloadIndex

<b>DWORD</b> containing the payload index. This identifies the payload item to which this fragment belongs.


### -field segmentData

A <b>WMT_BUFFER_SEGMENT</b> structure specifying the buffer segment containing the payload fragment.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

