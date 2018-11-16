---
UID: NC:resapi.PSET_RESOURCE_STATUS_ROUTINE_EX
title: PSET_RESOURCE_STATUS_ROUTINE_EX
author: windows-sdk-content
description: Called to update the status of a resource.
old-location: mscs\setresourcestatusex.htm
tech.root: MsCS
ms.assetid: 3733F912-9D43-489B-91D8-7128D0F5D1A4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSET_RESOURCE_STATUS_ROUTINE_EX, PSET_RESOURCE_STATUS_ROUTINE_EX callback function [Failover Cluster], SetResourceStatusEx, SetResourceStatusEx callback, SetResourceStatusEx callback function [Failover Cluster], mscs.setresourcestatusex, resapi/PSET_RESOURCE_STATUS_ROUTINE_EX, resapi/SetResourceStatusEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SetResourceStatusEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSET_RESOURCE_STATUS_ROUTINE_EX callback function


## -description


Called to update the status of a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. 
    The <b>PSET_RESOURCE_STATUS_ROUTINE_EX</b> type defines a pointer to this function.


## -parameters




### -param ResourceHandle

A handle to the resource to be updated. The <i>ResourceHandle</i> parameter should 
       contain the same handle that is used for the <i>ResourceHandle</i> parameter in the 
       <a href="https://msdn.microsoft.com/EA798D15-9458-4F66-8D0E-13DA383552F7">OpenV2</a> entry point for this resource.


### -param ResourceStatus

A pointer to a <a href="https://msdn.microsoft.com/CBEBF870-B413-400C-A485-FD093358FB67">RESOURCE_STATUS_EX</a> structure that 
       contains information about the resource's state.


## -returns



One of 
       the following values of the 
       <a href="https://msdn.microsoft.com/d1b9fd8f-7d49-4396-8f0c-6db8fad5749e">RESOURCE_EXIT_STATE</a> enumeration.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ResourceExitStateContinue</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The resource has not been terminated. Worker threads can  continue 
         <a href="https://msdn.microsoft.com/0462CDFD-6499-4FF8-8B5C-4DC15AC30169">OnlineV2</a> and 
         <a href="https://msdn.microsoft.com/2983B328-08ED-4DA6-8DC2-79D44C710888">OfflineV2</a> operations for the resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ResourceExitStateTerminate</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The resource has been terminated. Callers should end 
         <a href="https://msdn.microsoft.com/0462CDFD-6499-4FF8-8B5C-4DC15AC30169">OnlineV2</a> or 
         <a href="https://msdn.microsoft.com/2983B328-08ED-4DA6-8DC2-79D44C710888">OfflineV2</a> operations and immediately terminate all worker 
         threads that are assigned to the resource.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

