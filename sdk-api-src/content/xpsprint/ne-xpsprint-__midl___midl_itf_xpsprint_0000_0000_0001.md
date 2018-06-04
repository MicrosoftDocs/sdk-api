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

# __MIDL___MIDL_itf_xpsprint_0000_0000_0001 enumeration


## -description


<p class="CCE_Message">[<b>XPS_JOB_COMPLETION</b> is not supported and may be altered or unavailable in the future. ]

Indicates the completion status of a print job.


## -enum-fields




### -field XPS_JOB_IN_PROGRESS

The print  job is running.


### -field XPS_JOB_COMPLETED

The print job finished without an error.


### -field XPS_JOB_CANCELLED

The print job was cancelled by a call to <a href="https://msdn.microsoft.com/f9fab578-95f0-498b-85ad-fd6ee2c72c63">IXpsPrintJob::Cancel</a>, or cancelled while it was being processed by the  print spooler.


### -field XPS_JOB_FAILED

The print job failed. The <b>jobStatus</b> member of <a href="https://msdn.microsoft.com/c4e13960-4f26-460a-b47e-98b833fcdfd5">XPS_JOB_STATUS</a> contains the error code of the failure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541159">Documents</a>



<a href="https://msdn.microsoft.com/e2a55aec-f8a5-40b4-8c26-1488df49eed0">IXpsPrintJob::GetJobStatus</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/c4e13960-4f26-460a-b47e-98b833fcdfd5">XPS_JOB_STATUS</a>
 

 

