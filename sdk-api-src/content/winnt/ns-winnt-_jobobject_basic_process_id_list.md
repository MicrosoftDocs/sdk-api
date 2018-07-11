---
UID: NS:winnt._JOBOBJECT_BASIC_PROCESS_ID_LIST
title: "_JOBOBJECT_BASIC_PROCESS_ID_LIST"
author: windows-sdk-content
description: Contains the process identifier list for a job object.
old-location: base\jobobject_basic_process_id_list_str.htm
old-project: ProcThread
ms.assetid: fae42f3b-d4bd-4126-aa19-47f046ced09f
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PJOBOBJECT_BASIC_PROCESS_ID_LIST, JOBOBJECT_BASIC_PROCESS_ID_LIST, JOBOBJECT_BASIC_PROCESS_ID_LIST structure, PJOBOBJECT_BASIC_PROCESS_ID_LIST, PJOBOBJECT_BASIC_PROCESS_ID_LIST structure pointer, _JOBOBJECT_BASIC_PROCESS_ID_LIST, _win32_jobobject_basic_process_id_list_str, base.jobobject_basic_process_id_list_str, winnt/JOBOBJECT_BASIC_PROCESS_ID_LIST, winnt/PJOBOBJECT_BASIC_PROCESS_ID_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: JOBOBJECT_BASIC_PROCESS_ID_LIST, *PJOBOBJECT_BASIC_PROCESS_ID_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - JOBOBJECT_BASIC_PROCESS_ID_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _JOBOBJECT_BASIC_PROCESS_ID_LIST structure


## -description


Contains the process identifier list for a job object. If the job is nested, the process identifier list consists of all processes associated with the job and its child jobs.


## -struct-fields




### -field NumberOfAssignedProcesses

The number of process identifiers to be stored in <b>ProcessIdList</b>.


### -field NumberOfProcessIdsInList

The number of process identifiers returned in the <b>ProcessIdList</b> buffer. If this number is less than <b>NumberOfAssignedProcesses</b>, increase the size of the buffer to accommodate the complete list.


### -field ProcessIdList

A variable-length array of process identifiers returned by this call. Array elements 0 through <b>NumberOfProcessIdsInList</b>
						– 1 contain valid process identifiers.


## -see-also




<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

