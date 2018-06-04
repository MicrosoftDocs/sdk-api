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

# CM_Get_Res_Des_Data_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538641">CM_Get_Res_Des_Data</a> instead.]

The <b>CM_Get_Res_Des_Data_Ex</b> function retrieves the information stored in a <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a> on a local or a remote machine.


## -parameters




### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff538603">CM_Get_Next_Res_Des_Ex</a>.


### -param Buffer [out]

Address of a buffer to receive the contents of a resource descriptor. The required buffer size should be obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538664">CM_Get_Res_Des_Data_Size_Ex</a>.


### -param BufferLen [in]

Caller-supplied length of the buffer specified by <i>Buffer</i>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Information returned in the buffer supplied by <i>Buffer</i> will be formatted as one of the resource type structures listed in the description of <a href="https://msdn.microsoft.com/library/windows/hardware/ff537941">CM_Add_Res_Des_Ex</a>, based on the resource type that was specified when <a href="https://msdn.microsoft.com/library/windows/hardware/ff538603">CM_Get_Next_Res_Des_Ex</a> was called to obtain the resource descriptor handle.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538641">CM_Get_Res_Des_Data</a>
 

 

