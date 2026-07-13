---
UID: NF:faxcomex.IFaxIncomingJob.get_JobType
title: IFaxIncomingJob::get_JobType (faxcomex.h)
description: Retrieves the JobType property of a FaxIncomingJob object. The JobType property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.
helpviewer_keywords: ["IFaxIncomingJob interface [Fax Service]","get_JobType method","IFaxIncomingJob.get_JobType","IFaxIncomingJob::get_JobType","_mfax_faxincomingjob.jobtype_cpp","fax._mfax_faxincomingjob_jobtype_cpp","faxcomex/IFaxIncomingJob::get_JobType","get_JobType","get_JobType method [Fax Service]","get_JobType method [Fax Service]","IFaxIncomingJob interface"]
old-location: fax\_mfax_faxincomingjob_jobtype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_965h_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_JobType method, IFaxIncomingJob.get_JobType, IFaxIncomingJob::get_JobType, _mfax_faxincomingjob.jobtype_cpp, fax._mfax_faxincomingjob_jobtype_cpp, faxcomex/IFaxIncomingJob::get_JobType, get_JobType, get_JobType method [Fax Service], get_JobType method [Fax Service],IFaxIncomingJob interface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxIncomingJob::get_JobType
 - faxcomex/IFaxIncomingJob::get_JobType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingJob.get_JobType
---

# IFaxIncomingJob::get_JobType


## -description

Retrieves the <b>JobType</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-jobtype">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.

## -parameters

### -param pJobType [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_type_enum">FAX_JOB_TYPE_ENUM</a>*</b>

Pointer to a value from the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_type_enum">FAX_JOB_TYPE_ENUM</a> enumeration that specifies the fax job type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-jobtype">JobType</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-queue">Visual Basic Example</a>