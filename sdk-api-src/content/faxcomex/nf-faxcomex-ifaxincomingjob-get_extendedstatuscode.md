---
UID: NF:faxcomex.IFaxIncomingJob.get_ExtendedStatusCode
title: IFaxIncomingJob::get_ExtendedStatusCode (faxcomex.h)
description: Retrieves the ExtendedStatusCode property of a FaxIncomingJob object. The ExtendedStatusCode property specifies a code describing the job's extended status.
helpviewer_keywords: ["IFaxIncomingJob interface [Fax Service]","get_ExtendedStatusCode method","IFaxIncomingJob.get_ExtendedStatusCode","IFaxIncomingJob::get_ExtendedStatusCode","_mfax_faxincomingjob.extendedstatuscode_cpp","fax._mfax_faxincomingjob_extendedstatuscode_cpp","faxcomex/IFaxIncomingJob::get_ExtendedStatusCode","get_ExtendedStatusCode","get_ExtendedStatusCode method [Fax Service]","get_ExtendedStatusCode method [Fax Service]","IFaxIncomingJob interface"]
old-location: fax\_mfax_faxincomingjob_extendedstatuscode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_40v9_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_ExtendedStatusCode method, IFaxIncomingJob.get_ExtendedStatusCode, IFaxIncomingJob::get_ExtendedStatusCode, _mfax_faxincomingjob.extendedstatuscode_cpp, fax._mfax_faxincomingjob_extendedstatuscode_cpp, faxcomex/IFaxIncomingJob::get_ExtendedStatusCode, get_ExtendedStatusCode, get_ExtendedStatusCode method [Fax Service], get_ExtendedStatusCode method [Fax Service],IFaxIncomingJob interface
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
 - IFaxIncomingJob::get_ExtendedStatusCode
 - faxcomex/IFaxIncomingJob::get_ExtendedStatusCode
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
 - IFaxIncomingJob.get_ExtendedStatusCode
---

# IFaxIncomingJob::get_ExtendedStatusCode


## -description

Retrieves the <b>ExtendedStatusCode</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <b>ExtendedStatusCode</b> property specifies a code describing the job's extended status.

## -parameters

### -param pExtendedStatusCode [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_extended_status_enum">FAX_JOB_EXTENDED_STATUS_ENUM</a>*</b>

Pointer to a value from the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_extended_status_enum">FAX_JOB_EXTENDED_STATUS_ENUM</a> enumeration that specifies the extended job status.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-extendedstatuscode">ExtendedStatusCode</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>