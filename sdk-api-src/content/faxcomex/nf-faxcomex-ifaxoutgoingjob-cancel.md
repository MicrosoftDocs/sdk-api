---
UID: NF:faxcomex.IFaxOutgoingJob.Cancel
title: IFaxOutgoingJob::Cancel
author: windows-sdk-content
description: The IFaxOutgoingJob::Cancel method cancels the outbound fax job.
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_cancel_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_827g.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Cancel, Cancel method [Fax Service], Cancel method [Fax Service],IFaxOutgoingJob interface, IFaxOutgoingJob interface [Fax Service],Cancel method, IFaxOutgoingJob.Cancel, IFaxOutgoingJob::Cancel, _mfax_faxoutgoingjob.cancel, fax._mfax_faxoutgoingjob_cancel, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_cancel_cpp, faxcomex/IFaxOutgoingJob::Cancel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJob.Cancel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingJob::Cancel


## -description


The <b>IFaxOutgoingJob::Cancel</b> method cancels the outbound fax job.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When you cancel a job that is not part of a broadcast or when you cancel an entire broadcast, the <a href="https://msdn.microsoft.com/904de452-446a-4dbf-9d32-b83f26a715bf">Count</a> property is updated to reflect the change in the number of outgoing jobs. However, if you cancel a single fax from a broadcast, the <b>Count</b> property does not reflect the change. The canceled fax remains in the outgoing queue, so that you can view the status of all faxes from the broadcast.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> or <b>farMANAGE_JOBS</b> access right. With the <b>farSUBMIT_LOW</b> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_JOBS</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/f9686d11-fd32-4eaf-ae93-399dacf028ac">FaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/5fab26c3-99f6-4740-9899-3dccbd26a3ba">Visual Basic Example</a>
 

 

