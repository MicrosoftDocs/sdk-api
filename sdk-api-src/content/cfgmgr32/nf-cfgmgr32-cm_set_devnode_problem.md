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

# CM_Set_DevNode_Problem function


## -description


The <b>CM_Set_DevNode_Problem</b> function sets a problem code for a device that is installed in a local machine.


## -parameters




### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulProblem [in]

Supplies a problem code, which is zero or one of the CM_PROB_Xxx flags that are described in <a href="devinst.device_manager_error_messages">Device Manager Error Messages</a>. A value of zero indicates that a problem is not set for the device. 


### -param ulFlags [in]

Must be set to zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



Use this function to set a problem code for a device that is installed in a local machine. You can also use the following functions to set a device's problem code and to obtain the problem code set for the device:

<ul>
<li>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a> returns the problem code set for a device installed in a local machine.

</li>
<li>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff538517">CM_Get_DevNode_Status_Ex</a> returns the problem code set for a device installed in a local or a remote machine.

</li>
<li>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539842">CM_Set_DevNode_Problem_Ex</a> sets a problem code for a device installed in a local or a remote machine.

</li>
</ul>
For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538074">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538517">CM_Get_DevNode_Status_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539842">CM_Set_DevNode_Problem_Ex</a>
 

 

