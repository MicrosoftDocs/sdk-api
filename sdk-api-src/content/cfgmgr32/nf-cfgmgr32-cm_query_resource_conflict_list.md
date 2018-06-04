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

# CM_Query_Resource_Conflict_List function


## -description


The <b>CM_Query_Resource_Conflict_List</b> function identifies device instances having resource requirements that conflict with a specified device instance's resource description.


## -parameters




### -param pclConflictList [out]

Caller-supplied address of a location to receive a handle to a conflict list.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.


### -param ResourceID [in]

Caller-supplied resource type identifier. This must be one of the <b>ResType_</b>-prefixed constants defined in <i>Cfgmgr32.h</i>.


### -param ResourceData [in]

Caller-supplied pointer to a resource descriptor, which can be one of the structures listed under the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537939">CM_Add_Res_Des</a> function's description of <i>ResourceData</i>.


### -param ResourceLen [in]

Caller-supplied length of the structure pointed to by <i>ResourceData</i>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Query_Resource_Conflict_List</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



When calling <b>CM_Query_Resource_Conflict_List</b>, specify a device instance handle and resource descriptor. (Resource descriptors for existing device nodes can be obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538641">CM_Get_Res_Des_Data</a>.) These parameters indicate the specific resources you'd like a specific device to use. The resulting conflict list identifies devices that use the same resources, along with resources reserved by the machine.

After calling <b>CM_Query_Resource_Conflict_List</b>, an application can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538622">CM_Get_Resource_Conflict_Count</a> to determine the number of conflicts contained in the resource conflict list. (The number of conflicts can be zero.) Then the application can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538631">CM_Get_Resource_Conflict_Details</a> for each entry in the conflict list.

After an application has finished using the handle received for <i>pclConflictList</i>, it must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538056">CM_Free_Resource_Conflict_Handle</a>.

For information about using device instance handles that are bound to a local or a remote machine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538076">CM_Get_Child_Ex</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538056">CM_Free_Resource_Conflict_Handle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538076">CM_Get_Child_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538641">CM_Get_Res_Des_Data</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538622">CM_Get_Resource_Conflict_Count</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538631">CM_Get_Resource_Conflict_Details</a>
 

 

