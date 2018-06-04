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

# _JOBOBJECT_END_OF_JOB_TIME_INFORMATION structure


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
<a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a> function. After the completion packet is posted, the system clears the end-of-job time limit, and processes in the job can continue their execution. 




If no completion port is associated with the job when the time limit has been exceeded, the action taken is the same as for JOB_OBJECT_TERMINATE_AT_END_OF_JOB.

</td>
</tr>
</table>
 


## -remarks



The end-of-job time limit is specified in the <b>PerJobUserTimeLimit</b> member of the 
<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure.

To associate a completion port with a job, use the 
<a href="https://msdn.microsoft.com/18120d81-5480-4e0d-8422-0366a6811319">JOBOBJECT_ASSOCIATE_COMPLETION_PORT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/18120d81-5480-4e0d-8422-0366a6811319">JOBOBJECT_ASSOCIATE_COMPLETION_PORT</a>



<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

