---
UID: NF:jobapi2.QueryIoRateControlInformationJobObject
title: QueryIoRateControlInformationJobObject function (jobapi2.h)
description: Gets information about the control of the I/O rate for a job object.
helpviewer_keywords: ["QueryIoRateControlInformationJobObject","QueryIoRateControlInformationJobObject function","base.queryioratecontrolinformationjobobject","jobapi2/QueryIoRateControlInformationJobObject"]
old-location: base\queryioratecontrolinformationjobobject.htm
tech.root: backup
ms.assetid: B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC
ms.date: 01/09/2025
ms.keywords: QueryIoRateControlInformationJobObject, QueryIoRateControlInformationJobObject function, base.queryioratecontrolinformationjobobject, jobapi2/QueryIoRateControlInformationJobObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryIoRateControlInformationJobObject
 - jobapi2/QueryIoRateControlInformationJobObject
dev_langs:
 - c++
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
---

# QueryIoRateControlInformationJobObject function


## -description

**Windows 10, version 1607, and newer: This function is not supported.**

Gets information about the control of the I/O rate for a job object.

## -parameters

### -param hJob [in, optional]

A handle to the job to query for information. Get this handle from the <a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a> or <a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a> function. The handle must have the <b>JOB_OBJECT_QUERY</b> access right. For more information about access rights, see <a href="/windows/desktop/ProcThread/job-object-security-and-access-rights">Job Object Security and Access Rights</a>.

If this value is NULL and the process that calls <b>QueryIoRateControlInformationJobObject</b> is associated with a job, the function uses job that is associated with the process. If the job is nested within another job, the function uses the immediate job for the process.

### -param VolumeName [in, optional]

The name of the volume to query. If this value is NULL, the function gets the information about I/O rate control for the job for all of the volumes for the system.

### -param InfoBlocks [out]

A pointer to array of <a href="/windows/desktop/api/jobapi2/ns-jobapi2-jobobject_io_rate_control_information">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a> structures that contain the information about I/O rate control for the job. Your code must free the memory for this array by calling the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-freememoryjobobject">FreeMemoryJobObject</a> function with the address of the array.

### -param InfoBlockCount [out]

The number of <a href="/windows/desktop/api/jobapi2/ns-jobapi2-jobobject_io_rate_control_information">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a> structures that the function allocated in the array to which the <i>InfoBlocks</i> parameter points.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-freememoryjobobject">FreeMemoryJobObject</a>



<a href="/windows/desktop/api/jobapi2/ns-jobapi2-jobobject_io_rate_control_information">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setioratecontrolinformationjobobject">SetIoRateControlInformationJobObject</a>