---
UID: NF:xpsprint.IXpsPrintJob.GetJobStatus
title: IXpsPrintJob::GetJobStatus (xpsprint.h)
author: windows-sdk-content
description: Gets the current status of the print job.
old-location: gdi\ixpsprintjob_getjobstatus.htm
tech.root: printdocs
ms.assetid: e2a55aec-f8a5-40b4-8c26-1488df49eed0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetJobStatus, GetJobStatus method [Windows GDI], GetJobStatus method [Windows GDI],IXpsPrintJob interface, IXpsPrintJob interface [Windows GDI],GetJobStatus method, IXpsPrintJob.GetJobStatus, IXpsPrintJob::GetJobStatus, gdi.ixpsprintjob_getjobstatus, xpsprint/IXpsPrintJob::GetJobStatus
ms.topic: method
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.h
api_name:
 - IXpsPrintJob.GetJobStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsPrintJob::GetJobStatus


## -description


<p class="CCE_Message">[IXpsPrintJob::GetJobSatus is not supported and may be altered or unavailable in the future. ]

Gets the current status of the print job.


## -parameters




### -param jobStatus [out, retval]

The current status of the print job. For information about the data that is returned in this structure, see <a href="https://msdn.microsoft.com/en-us/library/Dd374577(v=VS.85).aspx">XPS_JOB_STATUS</a>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<b>GetJobStatus</b> may be called during the print job processing or after the print job has completed. The values returned in <a href="https://msdn.microsoft.com/en-us/library/Dd374577(v=VS.85).aspx">XPS_JOB_STATUS</a> represent   the current state of the print job at the time <b>GetJobStatus</b> is called, so it is possible to miss intermediate states between calls to this method.

The values of <i>jobStatus.currentDocument</i> and <i>jobStatus.currentPage</i> are guaranteed to progress sequentially: from the first document to the last,  and  from the first page to the last within each document.

The job ID of a print job that has been  sent to the Microsoft XPS Document Writer (MXDW) is zero. If the interface is that of a print job that has been sent to the MXDW,  zero will be returned in <i>jobStatus.jobId</i>.

If no job ID has been assigned to the print job, or the print job is printed without spooling, zero will be returned in <i>jobStatus.jobId</i>.




## -see-also




<a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">Documents</a>



<a href="https://msdn.microsoft.com/aa17e059-6208-4348-87f3-556a3818f2b9">IXpsPrintJob</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd374575(v=VS.85).aspx">XPS_JOB_COMPLETION</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd374577(v=VS.85).aspx">XPS_JOB_STATUS</a>
 

 

