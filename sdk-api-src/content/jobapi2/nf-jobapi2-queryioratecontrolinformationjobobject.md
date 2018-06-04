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

# QueryIoRateControlInformationJobObject function


## -description


Gets information about the control of the I/O rate for a job object.


## -parameters




### -param hJob [in, optional]

A handle to the job to query for information. Get this handle from the <a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a> or <a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a> function. The handle must have the <b>JOB_OBJECT_QUERY</b> access right. For more information about access rights, see <a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">Job Object Security and Access Rights</a>.

If this value is NULL and the process that calls <b>QueryIoRateControlInformationJobObject</b> is associated with a job, the function uses job that is associated with the process. If the job is nested within another job, the function uses the immediate job for the process.


### -param VolumeName [in, optional]

The name of the volume to query. If this value is NULL, the function gets the information about I/O rate control for the job for all of the volumes for the system.


### -param InfoBlocks [out]

A pointer to array of <a href="https://msdn.microsoft.com/E4AA03B5-4D83-4826-B85D-FA4B412AFEBF">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a> structures that contain the information about I/O rate control for the job. Your code must free the memory for this array by calling the <a href="https://msdn.microsoft.com/8EA45FC6-A8CC-4786-8CF2-4FC868B974F2">FreeMemoryJobObject</a> function with the address of the array. 


### -param InfoBlockCount [out]

The number of <a href="https://msdn.microsoft.com/E4AA03B5-4D83-4826-B85D-FA4B412AFEBF">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a> structures that the function allocated in the array to which the <i>InfoBlocks</i> parameter points.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<div class="alert"><b>Important</b>  Starting with Windows 10, version 1607, this function is no longer supported.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8EA45FC6-A8CC-4786-8CF2-4FC868B974F2">FreeMemoryJobObject</a>



<a href="https://msdn.microsoft.com/E4AA03B5-4D83-4826-B85D-FA4B412AFEBF">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a>



<a href="https://msdn.microsoft.com/7E108E01-6D43-4336-BFE0-5EE655FD5D45">SetIoRateControlInformationJobObject</a>
 

 

