---
UID: NF:faxcomex.IFaxIncomingJob.Cancel
title: IFaxIncomingJob::Cancel (faxcomex.h)
description: The Cancel method cancels the incoming fax job.
helpviewer_keywords: ["Cancel","Cancel method [Fax Service]","Cancel method [Fax Service]","IFaxIncomingJob interface","IFaxIncomingJob interface [Fax Service]","Cancel method","IFaxIncomingJob.Cancel","IFaxIncomingJob::Cancel","_mfax_faxincomingjob.cancel","fax._mfax_faxincomingjob_cancel","fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_cancel_cpp","faxcomex/IFaxIncomingJob::Cancel"]
old-location: fax\_mfax_faxincomingjob_cpp_mfax_faxincomingjob_cancel_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6g4s.htm
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Fax Service], Cancel method [Fax Service],IFaxIncomingJob interface, IFaxIncomingJob interface [Fax Service],Cancel method, IFaxIncomingJob.Cancel, IFaxIncomingJob::Cancel, _mfax_faxincomingjob.cancel, fax._mfax_faxincomingjob_cancel, fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_cancel_cpp, faxcomex/IFaxIncomingJob::Cancel
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
 - IFaxIncomingJob::Cancel
 - faxcomex/IFaxIncomingJob::Cancel
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
 - IFaxIncomingJob.Cancel
---

# IFaxIncomingJob::Cancel


## -description

The <b>Cancel</b> method cancels the incoming fax job.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_JOBS</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-queue">Visual Basic Example</a>
