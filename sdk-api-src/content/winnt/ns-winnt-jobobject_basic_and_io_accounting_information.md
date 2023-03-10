---
UID: NS:winnt._JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
title: JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION (winnt.h)
description: Contains basic accounting and I/O accounting information for a job object.
helpviewer_keywords: ["*PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION","JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION","JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION structure","PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION","PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION structure pointer","_JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION","_win32_jobobject_basic_and_io_accounting_information_str","base.jobobject_basic_and_io_accounting_information_str","winnt/JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION","winnt/PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION"]
old-location: base\jobobject_basic_and_io_accounting_information_str.htm
tech.root: backup
ms.assetid: 5c3e4002-d4d2-4a8c-ab0c-f6bcdd62947a
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION, JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION, JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION structure, PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION, PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION structure pointer, _JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION, _win32_jobobject_basic_and_io_accounting_information_str, base.jobobject_basic_and_io_accounting_information_str, winnt/JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION, winnt/PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION'
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
req.typenames: JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION, *PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
 - winnt/_JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
 - PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
 - winnt/PJOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
 - JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
 - winnt/JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
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
 - JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION
---

# JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION structure


## -description

Contains basic accounting and I/O accounting information for a job object.

## -struct-fields

### -field BasicInfo

A 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_accounting_information">JOBOBJECT_BASIC_ACCOUNTING_INFORMATION</a> structure that specifies the basic accounting information for the job.

### -field IoInfo

An 
<a href="/windows/desktop/api/winnt/ns-winnt-io_counters">IO_COUNTERS</a> structure that specifies the I/O accounting information for the job. The structure includes information for all processes that have ever been associated with the job, in addition to the information for all processes currently associated with the job.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-io_counters">IO_COUNTERS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_accounting_information">JOBOBJECT_BASIC_ACCOUNTING_INFORMATION</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>