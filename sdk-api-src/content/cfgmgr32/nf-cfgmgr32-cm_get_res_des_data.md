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

# CM_Get_Res_Des_Data function


## -description


The <b>CM_Get_Res_Des_Data</b> function retrieves the information stored in a <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a> on the local machine.


## -parameters




### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff538600">CM_Get_Next_Res_Des</a>.


### -param Buffer [out]

Address of a buffer to receive the contents of a resource descriptor. The required buffer size should be obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538658">CM_Get_Res_Des_Data_Size</a>.


### -param BufferLen [in]

Caller-supplied length of the buffer specified by <i>Buffer</i>.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Information returned in the buffer supplied by <i>Buffer</i> will be formatted as one of the resource type structures listed in the description of <a href="https://msdn.microsoft.com/library/windows/hardware/ff537939">CM_Add_Res_Des</a>, based on the resource type that was specified when <a href="https://msdn.microsoft.com/library/windows/hardware/ff538600">CM_Get_Next_Res_Des</a> was called to obtain the resource descriptor handle.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538649">CM_Get_Res_Des_Data_Ex</a>
 

 

