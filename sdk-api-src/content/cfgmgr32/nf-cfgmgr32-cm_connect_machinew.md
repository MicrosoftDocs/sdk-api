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

# CM_Connect_MachineW function


## -description


<p class="CCE_Message">[Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed. You cannot access remote machines when running on these versions of Windows.]

The <b>CM_Connect_Machine</b> function creates a connection to a remote machine.




## -parameters




### -param UNCServerName [in, optional]

Caller-supplied pointer to a text string representing the UNC name, including the <b>\\</b> prefix, of the system for which a connection will be made. If the pointer is <b>NULL</b>, the local system is used.


### -param phMachine [out]

Address of a location to receive a machine handle.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Callers of <b>CM_Connect_Machine</b> must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538005">CM_Disconnect_Machine</a> to deallocate the machine handle, after it is no longer needed.

Use machine handles obtained with this function only with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549713">PnP configuration manager functions</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538005">CM_Disconnect_Machine</a>
 

 

