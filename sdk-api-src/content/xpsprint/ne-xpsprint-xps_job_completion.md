---
UID: NE:xpsprint.__MIDL___MIDL_itf_xpsprint_0000_0000_0001
title: XPS_JOB_COMPLETION (xpsprint.h)
description: Indicates the completion status of a print job.
helpviewer_keywords: ["XPS_JOB_CANCELLED","XPS_JOB_COMPLETED","XPS_JOB_COMPLETION","XPS_JOB_COMPLETION enumeration [Windows GDI]","XPS_JOB_FAILED","XPS_JOB_IN_PROGRESS","gdi.xps_job_completion","xpsprint/XPS_JOB_CANCELLED","xpsprint/XPS_JOB_COMPLETED","xpsprint/XPS_JOB_COMPLETION","xpsprint/XPS_JOB_FAILED","xpsprint/XPS_JOB_IN_PROGRESS"]
old-location: gdi\xps_job_completion.htm
tech.root: xps
ms.assetid: a0bfb708-033a-4493-a878-0ebdcaae672f
ms.date: 12/05/2018
ms.keywords: XPS_JOB_CANCELLED, XPS_JOB_COMPLETED, XPS_JOB_COMPLETION, XPS_JOB_COMPLETION enumeration [Windows GDI], XPS_JOB_FAILED, XPS_JOB_IN_PROGRESS, gdi.xps_job_completion, xpsprint/XPS_JOB_CANCELLED, xpsprint/XPS_JOB_COMPLETED, xpsprint/XPS_JOB_COMPLETION, xpsprint/XPS_JOB_FAILED, xpsprint/XPS_JOB_IN_PROGRESS
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
req.typenames: XPS_JOB_COMPLETION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsprint_0000_0000_0001
 - xpsprint/__MIDL___MIDL_itf_xpsprint_0000_0000_0001
 - XPS_JOB_COMPLETION
 - xpsprint/XPS_JOB_COMPLETION
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
 - XPS_JOB_COMPLETION
---

# XPS_JOB_COMPLETION enumeration


## -description

<p class="CCE_Message">[<b>XPS_JOB_COMPLETION</b> is not supported and may be altered or unavailable in the future. ]

Indicates the completion status of a print job.

## -enum-fields

### -field XPS_JOB_IN_PROGRESS:0

The print  job is running.

### -field XPS_JOB_COMPLETED

The print job finished without an error.

### -field XPS_JOB_CANCELLED

The print job was cancelled by a call to <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-cancel">IXpsPrintJob::Cancel</a>, or cancelled while it was being processed by the  print spooler.

### -field XPS_JOB_FAILED

The print job failed. The <b>jobStatus</b> member of <a href="/windows/win32/api/xpsprint/ns-xpsprint-xps_job_status">XPS_JOB_STATUS</a> contains the error code of the failure.

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a>



<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>



<a href="/windows/win32/api/xpsprint/ns-xpsprint-xps_job_status">XPS_JOB_STATUS</a>
