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

# IXpsPrintJob::GetJobStatus


## -description


<p class="CCE_Message">[IXpsPrintJob::GetJobSatus is not supported and may be altered or unavailable in the future. ]

Gets the current status of the print job.


## -parameters




### -param jobStatus [out, retval]

The current status of the print job. For information about the data that is returned in this structure, see <a href="https://msdn.microsoft.com/c4e13960-4f26-460a-b47e-98b833fcdfd5">XPS_JOB_STATUS</a>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<b>GetJobStatus</b> may be called during the print job processing or after the print job has completed. The values returned in <a href="https://msdn.microsoft.com/c4e13960-4f26-460a-b47e-98b833fcdfd5">XPS_JOB_STATUS</a> represent   the current state of the print job at the time <b>GetJobStatus</b> is called, so it is possible to miss intermediate states between calls to this method.

The values of <i>jobStatus.currentDocument</i> and <i>jobStatus.currentPage</i> are guaranteed to progress sequentially: from the first document to the last,  and  from the first page to the last within each document.

The job ID of a print job that has been  sent to the Microsoft XPS Document Writer (MXDW) is zero. If the interface is that of a print job that has been sent to the MXDW,  zero will be returned in <i>jobStatus.jobId</i>.

If no job ID has been assigned to the print job, or the print job is printed without spooling, zero will be returned in <i>jobStatus.jobId</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541159">Documents</a>



<a href="https://msdn.microsoft.com/aa17e059-6208-4348-87f3-556a3818f2b9">IXpsPrintJob</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/a0bfb708-033a-4493-a878-0ebdcaae672f">XPS_JOB_COMPLETION</a>



<a href="https://msdn.microsoft.com/c4e13960-4f26-460a-b47e-98b833fcdfd5">XPS_JOB_STATUS</a>
 

 

