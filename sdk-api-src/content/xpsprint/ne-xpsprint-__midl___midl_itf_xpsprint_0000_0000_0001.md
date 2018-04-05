---
UID: NE:xpsprint.__MIDL___MIDL_itf_xpsprint_0000_0000_0001
title: "__MIDL___MIDL_itf_xpsprint_0000_0000_0001"
author: windows-driver-content
description: Indicates the completion status of a print job.
old-location: gdi\xps_job_completion.htm
old-project: printdocs
ms.assetid: a0bfb708-033a-4493-a878-0ebdcaae672f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: XPS_JOB_CANCELLED, XPS_JOB_COMPLETED, XPS_JOB_COMPLETION, XPS_JOB_COMPLETION enumeration [Windows GDI], XPS_JOB_FAILED, XPS_JOB_IN_PROGRESS, __MIDL___MIDL_itf_xpsprint_0000_0000_0001, gdi.xps_job_completion, xpsprint/XPS_JOB_CANCELLED, xpsprint/XPS_JOB_COMPLETED, xpsprint/XPS_JOB_COMPLETION, xpsprint/XPS_JOB_FAILED, xpsprint/XPS_JOB_IN_PROGRESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_1.idl; XpsObjectModel_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_JOB_COMPLETION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	XpsPrint.h
api_name:
-	XPS_JOB_COMPLETION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

