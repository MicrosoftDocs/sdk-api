---
UID: NF:jobapi2.SetIoRateControlInformationJobObject
title: SetIoRateControlInformationJobObject function (jobapi2.h)
description: Sets I/O limits on a job object.
helpviewer_keywords: ["SetIoRateControlInformationJobObject","SetIoRateControlInformationJobObject function","base.setioratecontrolinformationjobobject","jobapi2/SetIoRateControlInformationJobObject"]
old-location: base\setioratecontrolinformationjobobject.htm
tech.root: backup
ms.assetid: 7E108E01-6D43-4336-BFE0-5EE655FD5D45
ms.date: 01/09/2025
ms.keywords: SetIoRateControlInformationJobObject, SetIoRateControlInformationJobObject function, base.setioratecontrolinformationjobobject, jobapi2/SetIoRateControlInformationJobObject
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
 - SetIoRateControlInformationJobObject
 - jobapi2/SetIoRateControlInformationJobObject
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
 - SetIoRateControlInformationJobObject
---

# SetIoRateControlInformationJobObject function


## -description

**Windows 10, version 1607, and newer: This function is not supported.**

Sets I/O limits on a job object.

## -parameters

### -param hJob [in]

A handle to the job on which to set I/O limits. Get this handle from the <a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a> or <a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a> function. The handle must have the <b>JOB_OBJECT_SET_ATTRIBUTES</b> access right. For more information about access rights, see <a href="/windows/desktop/ProcThread/job-object-security-and-access-rights">Job Object Security and Access Rights</a>.

### -param IoRateControlInfo [in]

A pointer to a <a href="/windows/desktop/api/jobapi2/ns-jobapi2-jobobject_io_rate_control_information">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a> structure that specifies the I/O limits to set for the job.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

## -see-also

<a href="/windows/desktop/api/jobapi2/ns-jobapi2-jobobject_io_rate_control_information">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryioratecontrolinformationjobobject">QueryIoRateControlInformationJobObject</a>