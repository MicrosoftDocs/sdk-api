---
UID: NS:winnt._JOBOBJECT_BASIC_PROCESS_ID_LIST
title: JOBOBJECT_BASIC_PROCESS_ID_LIST (winnt.h)
description: Contains the process identifier list for a job object.
helpviewer_keywords: ["*PJOBOBJECT_BASIC_PROCESS_ID_LIST","JOBOBJECT_BASIC_PROCESS_ID_LIST","JOBOBJECT_BASIC_PROCESS_ID_LIST structure","PJOBOBJECT_BASIC_PROCESS_ID_LIST","PJOBOBJECT_BASIC_PROCESS_ID_LIST structure pointer","_JOBOBJECT_BASIC_PROCESS_ID_LIST","_win32_jobobject_basic_process_id_list_str","base.jobobject_basic_process_id_list_str","winnt/JOBOBJECT_BASIC_PROCESS_ID_LIST","winnt/PJOBOBJECT_BASIC_PROCESS_ID_LIST"]
old-location: base\jobobject_basic_process_id_list_str.htm
tech.root: backup
ms.assetid: fae42f3b-d4bd-4126-aa19-47f046ced09f
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_BASIC_PROCESS_ID_LIST, JOBOBJECT_BASIC_PROCESS_ID_LIST, JOBOBJECT_BASIC_PROCESS_ID_LIST structure, PJOBOBJECT_BASIC_PROCESS_ID_LIST, PJOBOBJECT_BASIC_PROCESS_ID_LIST structure pointer, _JOBOBJECT_BASIC_PROCESS_ID_LIST, _win32_jobobject_basic_process_id_list_str, base.jobobject_basic_process_id_list_str, winnt/JOBOBJECT_BASIC_PROCESS_ID_LIST, winnt/PJOBOBJECT_BASIC_PROCESS_ID_LIST'
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
req.typenames: JOBOBJECT_BASIC_PROCESS_ID_LIST, *PJOBOBJECT_BASIC_PROCESS_ID_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_BASIC_PROCESS_ID_LIST
 - winnt/_JOBOBJECT_BASIC_PROCESS_ID_LIST
 - PJOBOBJECT_BASIC_PROCESS_ID_LIST
 - winnt/PJOBOBJECT_BASIC_PROCESS_ID_LIST
 - JOBOBJECT_BASIC_PROCESS_ID_LIST
 - winnt/JOBOBJECT_BASIC_PROCESS_ID_LIST
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
 - JOBOBJECT_BASIC_PROCESS_ID_LIST
---

# JOBOBJECT_BASIC_PROCESS_ID_LIST structure


## -description

Contains the process identifier list for a job object. If the job is nested, the process identifier list consists of all processes associated with the job and its child jobs.

## -struct-fields

### -field NumberOfAssignedProcesses

The number of process identifiers to be stored in <b>ProcessIdList</b>.

### -field NumberOfProcessIdsInList

The number of process identifiers returned in the <b>ProcessIdList</b> buffer. If this number is less than <b>NumberOfAssignedProcesses</b>, increase the size of the buffer to accommodate the complete list.

### -field ProcessIdList

A variable-length array of process identifiers returned by this call. Array elements 0 through <b>NumberOfProcessIdsInList</b>– 1 contain valid process identifiers.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>