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

# CM_Is_Dock_Station_Present function


## -description


The <b>CM_Is_Dock_Station_Present</b> function identifies whether a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">docking station</a> is present in a local machine.


## -parameters




### -param pbPresent [out]

Pointer to a Boolean value that indicates whether a docking station is present in a local machine. The function sets *<i>pbPresen</i>t to <b>TRUE</b> if a docking station is present. Otherwise, the function sets *<i>pbPresen</i>t to <b>FALSE</b>.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



Use this function to determine whether a docking station is present in a local machine. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff538724">CM_Is_Dock_Station_Present_Ex</a> identifies whether a docking station is present in a local or a remote machine.

</li>
<li>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539811">CM_Request_Eject_PC</a> requests that a portable PC, which is inserted in a local docking station, be ejected.

</li>
<li>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539815">CM_Request_Eject_PC_Ex</a> requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538724">CM_Is_Dock_Station_Present_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539811">CM_Request_Eject_PC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539815">CM_Request_Eject_PC_Ex</a>
 

 

