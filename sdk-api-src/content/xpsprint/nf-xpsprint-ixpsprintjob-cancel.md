---
UID: NF:xpsprint.IXpsPrintJob.Cancel
title: IXpsPrintJob::Cancel
author: windows-sdk-content
description: Cancels the print job.
old-location: gdi\ixpsprintjob_cancel.htm
old-project: printdocs
ms.assetid: f9fab578-95f0-498b-85ad-fd6ee2c72c63
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: Cancel, Cancel method [Windows GDI], Cancel method [Windows GDI],IXpsPrintJob interface, IXpsPrintJob interface [Windows GDI],Cancel method, IXpsPrintJob.Cancel, IXpsPrintJob::Cancel, gdi.ixpsprintjob_cancel, xpsprint/IXpsPrintJob::Cancel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XPS_JOB_COMPLETION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.h
api_name:
 - IXpsPrintJob.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsPrintJob::Cancel


## -description


<p class="CCE_Message">[IXpsPrintJob::Cancel is not supported and may be altered or unavailable in the future. ]

Cancels the print job.


## -parameters






## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Any spooling or printing that is in progress at the time this method is called will be canceled.

This function is thread-safe and synchronized with the job status of the print job object.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541159">Documents</a>



<a href="https://msdn.microsoft.com/aa17e059-6208-4348-87f3-556a3818f2b9">IXpsPrintJob</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

