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

# CM_Get_Next_Res_Des_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538600">CM_Get_Next_Res_Des</a> instead.]

The <b>CM_Get_Next_Res_Des_Ex</b> function obtains a handle to the next <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a>, of a specified resource type, for a <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a> on a local or a remote machine.


## -parameters




### -param prdResDes [out]

Pointer to a location to receive a resource descriptor handle.


### -param rdResDes [in]

Caller-supplied handle to either a resource descriptor or a logical configuration. For more information, see the following <b>Remarks</b> section.


### -param ForResource [in]

Caller-supplied resource type identifier, indicating the type of resource descriptor being requested. This must be one of the ResType_-prefixed constants defined in <i>Cfgmgr32.h</i>.


### -param pResourceID [out, optional]

Pointer to a location to receive a resource type identifier, if <i>ForResource</i> specifies <b>ResType_All</b>. For any other <i>ForResource</i> value, callers should set this to <b>NULL</b>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Next_Res_Des_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



To enumerate a logical configuration's resource descriptors, begin by calling <b>CM_Get_Next_Res_Des_Ex</b> with the logical configuration's handle as the argument for <i>rdResDes</i>. This obtains a handle to the first resource descriptor of the type specified by <i>ForResource</i>. Then for each subsequent call to <b>CM_Get_Next_Res_Des_Ex</b>, specify the most recently obtained descriptor handle as the argument for <i>rdResDes</i>. Repeat until the function returns CR_NO_MORE_RES_DES.

To retrieve the information stored in a resource descriptor, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538649">CM_Get_Res_Des_Data_Ex</a>.

To modify the information stored in a resource descriptor, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538775">CM_Modify_Res_Des_Ex</a>.

Callers of <b>CM_Get_Next_Res_Des_Ex</b> must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538067">CM_Free_Res_Des_Handle</a> to deallocate the resource descriptor handle, after it is no longer needed.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538600">CM_Get_Next_Res_Des</a>
 

 

