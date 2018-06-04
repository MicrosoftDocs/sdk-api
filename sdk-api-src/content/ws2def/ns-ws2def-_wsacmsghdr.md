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

# _WSACMSGHDR structure


## -description


The CMSGHDR structure defines the header for a control data object that is associated with a
  datagram.


## -struct-fields




### -field cmsg_len

The number of bytes from the beginning of the CMSGHDR structure to the end of the control data.

<div class="alert"><b>Note</b>  The value of the 
      <b>cmsg_len</b> member does not account for any padding that may follow the
      control data.</div>
<div> </div>

### -field cmsg_level

The protocol that originated the control information.


### -field cmsg_type

The protocol-specific type of control information.


## -remarks



The control information data that is associated with a datagram is made up of one or more control data
    objects. Each object begins with a CMSGHDR structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff571164">WSK_DATAGRAM_INDICATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571141">WskReceiveFrom</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571148">WskSendTo</a>
 

 

