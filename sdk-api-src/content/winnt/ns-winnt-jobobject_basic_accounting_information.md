---
UID: NS:winnt._JOBOBJECT_BASIC_ACCOUNTING_INFORMATION
title: JOBOBJECT_BASIC_ACCOUNTING_INFORMATION (winnt.h)
description: Contains basic accounting information for a job object.
helpviewer_keywords: ["*PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION","JOBOBJECT_BASIC_ACCOUNTING_INFORMATION","JOBOBJECT_BASIC_ACCOUNTING_INFORMATION structure","PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION","PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION structure pointer","_JOBOBJECT_BASIC_ACCOUNTING_INFORMATION","_win32_jobobject_basic_accounting_information_str","base.jobobject_basic_accounting_information_str","winnt/JOBOBJECT_BASIC_ACCOUNTING_INFORMATION","winnt/PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION"]
old-location: base\jobobject_basic_accounting_information_str.htm
tech.root: backup
ms.assetid: 84dbe191-a5bf-4f55-815f-c4f2e60da22b
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION, JOBOBJECT_BASIC_ACCOUNTING_INFORMATION, JOBOBJECT_BASIC_ACCOUNTING_INFORMATION structure, PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION, PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION structure pointer, _JOBOBJECT_BASIC_ACCOUNTING_INFORMATION, _win32_jobobject_basic_accounting_information_str, base.jobobject_basic_accounting_information_str, winnt/JOBOBJECT_BASIC_ACCOUNTING_INFORMATION, winnt/PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: JOBOBJECT_BASIC_ACCOUNTING_INFORMATION, *PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_BASIC_ACCOUNTING_INFORMATION
 - winnt/_JOBOBJECT_BASIC_ACCOUNTING_INFORMATION
 - PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION
 - winnt/PJOBOBJECT_BASIC_ACCOUNTING_INFORMATION
 - JOBOBJECT_BASIC_ACCOUNTING_INFORMATION
 - winnt/JOBOBJECT_BASIC_ACCOUNTING_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - JOBOBJECT_BASIC_ACCOUNTING_INFORMATION
---

# JOBOBJECT_BASIC_ACCOUNTING_INFORMATION structure


## -description

Contains basic accounting information for a job object.

## -struct-fields

### -field TotalUserTime

The total amount of user-mode execution time for all active processes associated with the job, as well as all terminated processes no longer associated with the job, in 100-nanosecond ticks.

### -field TotalKernelTime

The total amount of kernel-mode execution time for all active processes associated with the job, as well as all terminated processes no longer associated with the job, in 100-nanosecond ticks.

### -field ThisPeriodTotalUserTime

The total amount of user-mode execution time for all active processes associated with the job (as well as all terminated processes no longer associated with the job) since the last call that set a per-job user-mode time limit, in 100-nanosecond ticks. 




This member is set to 0 on creation of the job, and each time a per-job user-mode time limit is established.

### -field ThisPeriodTotalKernelTime

The total amount of kernel-mode execution time for all active processes associated with the job (as well as all terminated processes no longer associated with the job) since the last call that set a per-job kernel-mode time limit, in 100-nanosecond ticks. 




This member is set to zero on creation of the job, and each time a per-job kernel-mode time limit is established.

### -field TotalPageFaultCount

The total number of page faults encountered by all active processes associated with the job, as well as all terminated processes no longer associated with the job.

### -field TotalProcesses

The total number of processes associated with the job during its lifetime, including those that have terminated. For example, when a process is associated with a job, but the association fails because of a limit violation, this value is incremented.

### -field ActiveProcesses

The total number of processes currently associated with the job. When a process is associated with a job, but the association fails because of a limit violation, this value is temporarily incremented. When the terminated process exits and all references to the process are released, this value is decremented.

### -field TotalTerminatedProcesses

The total number of processes terminated because of a limit violation.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>