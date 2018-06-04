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

# CM_Uninstall_DevNode function


## -description


The <b>CM_Uninstall_DevNode</b> function removes all persistent state associated with a device instance.


## -parameters




### -param dnDevInst [in]

Device instance handle that is bound to the local machine.


### -param ulFlags [in]

Reserved. Must be set to zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



This function uninstalls the device without sending an <b>IRP_MN_QUERY_REMOVE_DEVICE</b> request or calling class installers or co-installers.       If your application will run only on a <a href="https://docs.microsoft.com/windows-hardware/drivers/develop/windows-10-editions-for-universal-drivers">Target Platform</a> of Desktop, instead of calling <b>CM_Uninstall_DevNode</b>, the application should uninstall the device by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a> with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543717">DIF_REMOVE</a> code, or by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff544754">DiUninstallDevice</a>.

Use the following sequence to call this function:

<ol>
<li>Check if <a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a> returns success.  This means that the device is present.</li>
<li>If the device is present, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff539722">CM_Query_And_Remove_SubTree</a>.</li>
<li>Call <b>CM_Uninstall_DevNode</b>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

