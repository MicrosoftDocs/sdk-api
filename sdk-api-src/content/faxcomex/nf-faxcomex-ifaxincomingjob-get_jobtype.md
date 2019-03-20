---
UID: NF:faxcomex.IFaxIncomingJob.get_JobType
title: IFaxIncomingJob::get_JobType (faxcomex.h)
author: windows-sdk-content
description: Retrieves the JobType property of a FaxIncomingJob object. The JobType property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.
old-location: fax\_mfax_faxincomingjob_jobtype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_965h_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_JobType method, IFaxIncomingJob.get_JobType, IFaxIncomingJob::get_JobType, _mfax_faxincomingjob.jobtype_cpp, fax._mfax_faxincomingjob_jobtype_cpp, faxcomex/IFaxIncomingJob::get_JobType, get_JobType, get_JobType method [Fax Service], get_JobType method [Fax Service],IFaxIncomingJob interface
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
 - IFaxIncomingJob.get_JobType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJob::get_JobType


## -description


Retrieves the <b>JobType</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object. The <a href="https://msdn.microsoft.com/en-us/library/ms687471(v=VS.85).aspx">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.


## -parameters




### -param pJobType [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms689184(v=VS.85).aspx">FAX_JOB_TYPE_ENUM</a>*</b>

Pointer to a value from the <a href="https://msdn.microsoft.com/en-us/library/ms689184(v=VS.85).aspx">FAX_JOB_TYPE_ENUM</a> enumeration that specifies the fax job type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684878(v=VS.85).aspx">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687471(v=VS.85).aspx">JobType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692952(v=VS.85).aspx">Visual Basic Example</a>
 

 

