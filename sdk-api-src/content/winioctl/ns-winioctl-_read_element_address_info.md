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

# _READ_ELEMENT_ADDRESS_INFO structure


## -description


Represents the volume tag information. It is used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559417">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a> control code.


## -struct-fields




### -field NumberOfElements

The number of elements matching criteria set forth by the <b>ActionCode</b> member of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551479">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>. 




For information on compatibility with the current device, see the <b>Features0</b> member of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554979">GET_CHANGER_PARAMETERS</a>.


### -field ElementStatus

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551461">CHANGER_ELEMENT_STATUS</a> structures, one for each element that corresponded with the information passed in with the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551479">CHANGER_SEND_VOLUME_TAG_INFORMATION</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551461">CHANGER_ELEMENT_STATUS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551479">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559417">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a>
 

 

