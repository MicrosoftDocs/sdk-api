---
UID: NF:jobapi2.QueryIoRateControlInformationJobObject
title: QueryIoRateControlInformationJobObject function
author: windows-sdk-content
description: Gets information about the control of the I/O rate for a job object.
old-location: base\queryioratecontrolinformationjobobject.htm
tech.root: ProcThread
ms.assetid: B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: QueryIoRateControlInformationJobObject, QueryIoRateControlInformationJobObject function, base.queryioratecontrolinformationjobobject, jobapi2/QueryIoRateControlInformationJobObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: jobapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Job-L2-1-1.dll
 - Kernel32Legacy.dll
api_name:
 - QueryIoRateControlInformationJobObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

