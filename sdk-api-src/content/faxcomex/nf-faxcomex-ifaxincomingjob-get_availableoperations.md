---
UID: NF:faxcomex.IFaxIncomingJob.get_AvailableOperations
title: IFaxIncomingJob::get_AvailableOperations (faxcomex.h)
description: Retrieves the AvailableOperations property of a FaxIncomingJob object. The AvailableOperations property indicates the combination of valid operations that you can perform on the fax job given its current status.
helpviewer_keywords: ["IFaxIncomingJob interface [Fax Service]","get_AvailableOperations method","IFaxIncomingJob.get_AvailableOperations","IFaxIncomingJob::get_AvailableOperations","_mfax_faxincomingjob.availableoperations_cpp","fax._mfax_faxincomingjob_availableoperations_cpp","faxcomex/IFaxIncomingJob::get_AvailableOperations","get_AvailableOperations","get_AvailableOperations method [Fax Service]","get_AvailableOperations method [Fax Service]","IFaxIncomingJob interface"]
old-location: fax\_mfax_faxincomingjob_availableoperations_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0z1v_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],get_AvailableOperations method, IFaxIncomingJob.get_AvailableOperations, IFaxIncomingJob::get_AvailableOperations, _mfax_faxincomingjob.availableoperations_cpp, fax._mfax_faxincomingjob_availableoperations_cpp, faxcomex/IFaxIncomingJob::get_AvailableOperations, get_AvailableOperations, get_AvailableOperations method [Fax Service], get_AvailableOperations method [Fax Service],IFaxIncomingJob interface
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
 - IFaxIncomingJob::get_AvailableOperations
 - faxcomex/IFaxIncomingJob::get_AvailableOperations
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
 - IFaxIncomingJob.get_AvailableOperations
---

# IFaxIncomingJob::get_AvailableOperations


## -description

Retrieves the <b>AvailableOperations</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <b>AvailableOperations</b> property indicates the combination of valid operations that you can perform on the fax job given its current status.

## -parameters

### -param pAvailableOperations [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_operations_enum">FAX_JOB_OPERATIONS_ENUM</a>*</b>

Pointer to a <b>long</b> value from the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_operations_enum">FAX_JOB_OPERATIONS_ENUM</a> enumeration that specifies a bitwise combination of the operations that you can currently perform on the fax job. Some operations are mutually exclusive. For example, you cannot pause a job that has already been paused.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-availableoperations">AvailableOperations</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_job_operations_enum">FAX_JOB_OPERATIONS_ENUM</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>