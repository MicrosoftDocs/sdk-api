---
UID: NS:xpsprint.__MIDL___MIDL_itf_xpsprint_0000_0000_0002
title: XPS_JOB_STATUS (xpsprint.h)
description: Contains a snapshot of job status.
helpviewer_keywords: ["XPS_JOB_STATUS","XPS_JOB_STATUS structure [Windows GDI]","gdi.xps_job_status","xpsprint/XPS_JOB_STATUS"]
old-location: gdi\xps_job_status.htm
tech.root: xps
ms.assetid: c4e13960-4f26-460a-b47e-98b833fcdfd5
ms.date: 12/05/2018
ms.keywords: XPS_JOB_STATUS, XPS_JOB_STATUS structure [Windows GDI], gdi.xps_job_status, xpsprint/XPS_JOB_STATUS
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
targetos: Windows
req.typenames: XPS_JOB_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsprint_0000_0000_0002
 - xpsprint/__MIDL___MIDL_itf_xpsprint_0000_0000_0002
 - XPS_JOB_STATUS
 - xpsprint/XPS_JOB_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XpsPrint.h
api_name:
 - XPS_JOB_STATUS
---

# XPS_JOB_STATUS structure


## -description

<p class="CCE_Message">[<b>XPS_JOB_STATUS</b> is not supported and may be altered or unavailable in the future. ]

Contains a snapshot of job status.

## -struct-fields

### -field jobId

The spooler job ID that is assigned to the print job.  If no job ID has yet been assigned, <i>jobId</i> will be 0.

### -field currentDocument

The zero-based index of the most recently processed document in the print job;  0 is the first document, 1 is the next, and so on. If no documents have been processed, <i>currentDocument</i> will have a value of -1.

### -field currentPage

The zero-based index of the most recently processed page in the current document; 0 is the first page, 1 is the next, and so on. If no pages have been processed, <i>currentPage</i> will have a value of -1.

### -field currentPageTotal

A running total of the number of pages that have been processed by the print job. At the beginning of the job, this value is  0. As each page in each document is processed by the job, this value increases monotonically.

### -field completion

The <a href="/windows/win32/api/xpsprint/ne-xpsprint-xps_job_completion">XPS_JOB_COMPLETION</a> value that indicates the completion status of the job.  This value will change when the event passed in the <b>completionEvent</b> parameter of <a href="/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob">StartXpsPrintJob</a> is signaled at the end of a job. If the print job fails, this value will be <b>XPS_JOB_FAILED</b>,  with <i>jobStatus</i> containing the error code of the failure.

### -field jobStatus

The error state of the job.  If the job finishes without an error, this value will be <b>S_OK</b>. If an error causes the print job to exit, this value will be the error code of the failure.

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsprint/ne-xpsprint-xps_job_completion">XPS_JOB_COMPLETION</a>