---
UID: NS:winnt._JOBOBJECT_END_OF_JOB_TIME_INFORMATION
title: JOBOBJECT_END_OF_JOB_TIME_INFORMATION (winnt.h)
description: Specifies the action the system will perform when an end-of-job time limit is exceeded.
helpviewer_keywords: ["*PJOBOBJECT_END_OF_JOB_TIME_INFORMATION","JOBOBJECT_END_OF_JOB_TIME_INFORMATION","JOBOBJECT_END_OF_JOB_TIME_INFORMATION structure","JOB_OBJECT_POST_AT_END_OF_JOB","JOB_OBJECT_TERMINATE_AT_END_OF_JOB","PJOBOBJECT_END_OF_JOB_TIME_INFORMATION","PJOBOBJECT_END_OF_JOB_TIME_INFORMATION structure","_JOBOBJECT_END_OF_JOB_TIME_INFORMATION","_win32_jobobject_end_of_job_time_information_str","base.jobobject_end_of_job_time_information_str","winnt/JOBOBJECT_END_OF_JOB_TIME_INFORMATION","winnt/PJOBOBJECT_END_OF_JOB_TIME_INFORMATION"]
old-location: base\jobobject_end_of_job_time_information_str.htm
tech.root: backup
ms.assetid: 0054d018-c358-4cb0-a4db-fc6464b4b08c
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_END_OF_JOB_TIME_INFORMATION, JOBOBJECT_END_OF_JOB_TIME_INFORMATION, JOBOBJECT_END_OF_JOB_TIME_INFORMATION structure, JOB_OBJECT_POST_AT_END_OF_JOB, JOB_OBJECT_TERMINATE_AT_END_OF_JOB, PJOBOBJECT_END_OF_JOB_TIME_INFORMATION, PJOBOBJECT_END_OF_JOB_TIME_INFORMATION structure, _JOBOBJECT_END_OF_JOB_TIME_INFORMATION, _win32_jobobject_end_of_job_time_information_str, base.jobobject_end_of_job_time_information_str, winnt/JOBOBJECT_END_OF_JOB_TIME_INFORMATION, winnt/PJOBOBJECT_END_OF_JOB_TIME_INFORMATION'
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
req.typenames: JOBOBJECT_END_OF_JOB_TIME_INFORMATION, *PJOBOBJECT_END_OF_JOB_TIME_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_END_OF_JOB_TIME_INFORMATION
 - winnt/_JOBOBJECT_END_OF_JOB_TIME_INFORMATION
 - PJOBOBJECT_END_OF_JOB_TIME_INFORMATION
 - winnt/PJOBOBJECT_END_OF_JOB_TIME_INFORMATION
 - JOBOBJECT_END_OF_JOB_TIME_INFORMATION
 - winnt/JOBOBJECT_END_OF_JOB_TIME_INFORMATION
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
 - JOBOBJECT_END_OF_JOB_TIME_INFORMATION
---

# JOBOBJECT_END_OF_JOB_TIME_INFORMATION structure


## -description

Specifies the action the system will perform when an end-of-job time limit is exceeded.

## -struct-fields

### -field EndOfJobTimeAction

The action that the system will perform when the end-of-job time limit has been exceeded. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_TERMINATE_AT_END_OF_JOB"></a><a id="job_object_terminate_at_end_of_job"></a><dl>
<dt><b>JOB_OBJECT_TERMINATE_AT_END_OF_JOB</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Terminates all processes and sets the exit status to ERROR_NOT_ENOUGH_QUOTA. The processes cannot prevent or delay their own termination. The job object is set to the signaled state and remains signaled until this limit is reset. No additional processes can be assigned to the job until the limit is reset. 




This is the default termination action.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_POST_AT_END_OF_JOB"></a><a id="job_object_post_at_end_of_job"></a><dl>
<dt><b>JOB_OBJECT_POST_AT_END_OF_JOB</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Posts a completion packet to the completion port using the 
<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a> function. After the completion packet is posted, the system clears the end-of-job time limit, and processes in the job can continue their execution. 




If no completion port is associated with the job when the time limit has been exceeded, the action taken is the same as for JOB_OBJECT_TERMINATE_AT_END_OF_JOB.

</td>
</tr>
</table>

## -remarks

The end-of-job time limit is specified in the <b>PerJobUserTimeLimit</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure.

To associate a completion port with a job, use the 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_associate_completion_port">JOBOBJECT_ASSOCIATE_COMPLETION_PORT</a> structure.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_associate_completion_port">JOBOBJECT_ASSOCIATE_COMPLETION_PORT</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_BASIC_LIMIT_INFORMATION</a>



<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>