---
UID: NF:faxcomex.IFaxIncomingJob.get_JobType
title: IFaxIncomingJob::get_JobType method
author: windows-driver-content
description: Retrieves the JobType property of a FaxIncomingJob object. The JobType property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.
old-location: fax\_mfax_faxincomingjob_jobtype_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_965h_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxIncomingJob, IFaxIncomingJob interface [Fax Service], get_JobType method, IFaxIncomingJob::get_JobType, _mfax_faxincomingjob.jobtype_cpp, fax._mfax_faxincomingjob_jobtype_cpp, faxcomex/IFaxIncomingJob::get_JobType, get_JobType method [Fax Service], get_JobType method [Fax Service], IFaxIncomingJob interface, get_JobType,IFaxIncomingJob.get_JobType
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxIncomingJob.get_JobType
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingJob::get_JobType method


## -description


Retrieves the <b>JobType</b> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <a href="https://msdn.microsoft.com/53768e23-f93c-4fa7-b16e-23292f5a4380">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.


## -parameters




### -param pJobType [out, retval]

Type: <b><a href="https://msdn.microsoft.com/795b64ce-d2bb-4b33-bf69-4e78c873ffb2">FAX_JOB_TYPE_ENUM</a>*</b>

Pointer to a value from the <a href="https://msdn.microsoft.com/795b64ce-d2bb-4b33-bf69-4e78c873ffb2">FAX_JOB_TYPE_ENUM</a> enumeration that specifies the fax job type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/53768e23-f93c-4fa7-b16e-23292f5a4380">JobType</a>



<a href="https://msdn.microsoft.com/88cde2d4-09ee-4fbf-8a75-35de58dd45f5">Visual Basic Example</a>
 

 

