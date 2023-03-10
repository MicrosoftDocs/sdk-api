---
UID: NF:faxcomex.IFaxOutgoingJob.Cancel
title: IFaxOutgoingJob::Cancel (faxcomex.h)
description: The IFaxOutgoingJob::Cancel method cancels the outbound fax job.
helpviewer_keywords: ["Cancel","Cancel method [Fax Service]","Cancel method [Fax Service]","IFaxOutgoingJob interface","IFaxOutgoingJob interface [Fax Service]","Cancel method","IFaxOutgoingJob.Cancel","IFaxOutgoingJob::Cancel","_mfax_faxoutgoingjob.cancel","fax._mfax_faxoutgoingjob_cancel","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_cancel_cpp","faxcomex/IFaxOutgoingJob::Cancel"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_cancel_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_827g.htm
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Fax Service], Cancel method [Fax Service],IFaxOutgoingJob interface, IFaxOutgoingJob interface [Fax Service],Cancel method, IFaxOutgoingJob.Cancel, IFaxOutgoingJob::Cancel, _mfax_faxoutgoingjob.cancel, fax._mfax_faxoutgoingjob_cancel, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_cancel_cpp, faxcomex/IFaxOutgoingJob::Cancel
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
 - IFaxOutgoingJob::Cancel
 - faxcomex/IFaxOutgoingJob::Cancel
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
 - IFaxOutgoingJob.Cancel
---

# IFaxOutgoingJob::Cancel


## -description

The <b>IFaxOutgoingJob::Cancel</b> method cancels the outbound fax job.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When you cancel a job that is not part of a broadcast or when you cancel an entire broadcast, the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs-count-vb">Count</a> property is updated to reflect the change in the number of outgoing jobs. However, if you cancel a single fax from a broadcast, the <b>Count</b> property does not reflect the change. The canceled fax remains in the outgoing queue, so that you can view the status of all faxes from the broadcast.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farMANAGE_JOBS</b> access right. With the <b>farSUBMIT_LOW</b> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_JOBS</b> access right, users will be able to use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>
