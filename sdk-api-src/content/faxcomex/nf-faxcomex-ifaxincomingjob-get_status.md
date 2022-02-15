---
UID: NF:faxcomex.IFaxIncomingJob.get_Status
title: IFaxIncomingJob::get_Status (faxcomex.h)
description: Retrieves the Status property of a FaxIncomingJob object. The Status property is a number that indicates the current status of an inbound fax job in the job queue.
helpviewer_keywords: ["IFaxIncomingJob interface [Fax Service]","get_Status method","IFaxIncomingJob.get_Status","IFaxIncomingJob::get_Status","_mfax_faxincomingjob.status_cpp","fax._mfax_faxincomingjob_status_cpp","faxcomex/IFaxIncomingJob::get_Status","get_Status","get_Status method [Fax Service]","get_Status method [Fax Service]","IFaxIncomingJob interface"]
old-location: fax\_mfax_faxincomingjob_status_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1far_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_Status method, IFaxIncomingJob.get_Status, IFaxIncomingJob::get_Status, _mfax_faxincomingjob.status_cpp, fax._mfax_faxincomingjob_status_cpp, faxcomex/IFaxIncomingJob::get_Status, get_Status, get_Status method [Fax Service], get_Status method [Fax Service],IFaxIncomingJob interface
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
 - IFaxIncomingJob::get_Status
 - faxcomex/IFaxIncomingJob::get_Status
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
 - IFaxIncomingJob.get_Status
---

# IFaxIncomingJob::get_Status


## -description

Retrieves the <b>Status</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <b>Status</b> property is a number that indicates the current status of an inbound fax job in the job queue.

## -parameters

### -param pStatus [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_status_enum">FAX_JOB_STATUS_ENUM</a>*</b>

Pointer to a value from the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_status_enum">FAX_JOB_STATUS_ENUM</a> enumeration that specifies the current status of an inbound fax job in the job queue.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_status_enum">FAX_JOB_STATUS_ENUM</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-status">Status</a>