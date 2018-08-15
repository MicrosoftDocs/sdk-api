---
UID: NF:faxcomex.IFaxOutgoingJob.Cancel
title: IFaxOutgoingJob::Cancel
author: windows-sdk-content
description: The Cancel method cancels the outbound fax job.
old-location: fax\_mfax_faxoutgoingjob_cancel_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_827g.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Cancel, Cancel method [Fax Service], Cancel method [Fax Service],FaxOutgoingJob object, FaxOutgoingJob object [Fax Service],Cancel method, FaxOutgoingJob.Cancel, IFaxOutgoingJob.Cancel, IFaxOutgoingJob::Cancel, _mfax_faxoutgoingjob.cancel, fax._mfax_faxoutgoingjob_cancel, fax._mfax_faxoutgoingjob_cancel_vb
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingJob.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingJob::Cancel


## -description


The <b>Cancel</b> method cancels the outbound fax job.


## -parameters






## -remarks



When you cancel a job that is not part of a broadcast or when you cancel an entire broadcast, the <a href="https://msdn.microsoft.com/ba83bcc2-0e1a-47c4-9e37-0329010151eb">Count</a> property is updated to reflect the change in the number of outgoing jobs. However, if you cancel a single fax from a broadcast, the <b>Count</b> property does not reflect the change. The canceled fax remains in the outgoing queue, so that you can view the status of all faxes from the broadcast.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> or <b>farMANAGE_JOBS</b> access right. With the <b>farSUBMIT_LOW</b> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_JOBS</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/f9686d11-fd32-4eaf-ae93-399dacf028ac">FaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/5fab26c3-99f6-4740-9899-3dccbd26a3ba">Visual Basic Example</a>
 

 

