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

# _COPP_StatusFlags enumeration


## -description



Specifies the status of a Certified Output Protection Protocol (COPP) session.




## -enum-fields




### -field COPP_StatusNormal


            Normal status.
          


### -field COPP_LinkLost

The integrity of the connection has been compromised. Examples of events that cause the driver to set this flag include:

<ul>
<li>The driver can no longer enforce the current protection level.</li>
<li>The driver detected an internal integrity error.</li>
<li>The connector between the computer and the display device was unplugged.</li>
</ul>

### -field COPP_RenegotiationRequired


            The connection configuration has changed. For example, the user has changed the desktop display mode.
          


### -field COPP_StatusFlagsReserved


            Reserved. Must be zero.
          


## -remarks



If COPP_LinkLost is returned, the application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

