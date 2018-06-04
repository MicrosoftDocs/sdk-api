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

# GetDisplayConfigBufferSizes function


## -description


The <b>GetDisplayConfigBufferSizes</b> function retrieves the size of the buffers that are required to call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> function.


## -parameters




### -param flags

TBD


### -param numPathArrayElements

TBD


### -param numModeInfoArrayElements

TBD




#### - Flags [in]

The type of information to retrieve. The value for the <i>Flags</i> parameter must be one of the following values.





#### QDC_ALL_PATHS

The caller requests the table sizes to hold all the possible path combinations.



#### QDC_ONLY_ACTIVE_PATHS

The caller requests the table sizes to hold only active paths. 



#### QDC_DATABASE_CURRENT

The caller requests the table sizes to hold the active paths as defined in the persistence database for the currently connected monitors.


#### - pNumModeInfoArrayElements [out]

Pointer to a variable that receives the number of elements in the mode information table. The <i>pNumModeInfoArrayElements</i> parameter value is then used by a subsequent call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> function. This parameter cannot be <b>NULL</b>.


#### - pNumPathArrayElements [out]

Pointer to a variable that receives the number of elements in the path information table. The <i>pNumPathArrayElements</i> parameter value is then used by a subsequent call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> function. This parameter cannot be <b>NULL</b>.


## -returns



The function returns one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The combination of parameters and flags that are specified is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The system is not running a graphics driver that was written according to the <a href="https://msdn.microsoft.com/d9dc0d48-aea4-4614-a23b-e2449800469f">Windows Display Driver Model (WDDM)</a>. The function is only supported on a system with a WDDM driver running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access to the console session. This error occurs if the calling process does not have access to the current desktop or is running on a remote session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



Given the current display path configuration and the requested flags, <b>GetDisplayConfigBufferSizes</b> returns the size of the path and mode tables that are required to store the information. <b>GetDisplayConfigBufferSizes</b> can return values that are slightly larger than are actually required because it determines that all source and target paths are valid; whereas, the driver might place some restrictions on the possible combinations.

As <b>GetDisplayConfigBufferSizes</b> can only determine the required array size of that moment in time, it is possible that between calls to <b>GetDisplayConfigBufferSizes</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> the system configuration has changed and the provided array sizes are no longer sufficient to store the new path data. 

If a caller is aware that it must enable additional sources and targets, the caller can allocate a larger mode information array than is returned from <b>GetDisplayConfigBufferSizes</b> so that it has the space to add the additional source and target modes after calling <b>QueryDisplayConfig</b> and before calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a>
 

 

