---
UID: NF:faxcomex.IFaxIncomingJob.Refresh
title: IFaxIncomingJob::Refresh (faxcomex.h)
description: The Refresh method refreshes FaxIncomingJob object information from the fax server.
helpviewer_keywords: ["IFaxIncomingJob interface [Fax Service]","Refresh method","IFaxIncomingJob.Refresh","IFaxIncomingJob::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxIncomingJob interface","_mfax_faxincomingjob.refresh","fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_refresh_cpp","fax._mfax_faxincomingjob_refresh","faxcomex/IFaxIncomingJob::Refresh"]
old-location: fax\_mfax_faxincomingjob_cpp_mfax_faxincomingjob_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9fzc.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],Refresh method, IFaxIncomingJob.Refresh, IFaxIncomingJob::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingJob interface, _mfax_faxincomingjob.refresh, fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_refresh_cpp, fax._mfax_faxincomingjob_refresh, faxcomex/IFaxIncomingJob::Refresh
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
 - IFaxIncomingJob::Refresh
 - faxcomex/IFaxIncomingJob::Refresh
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
 - IFaxIncomingJob.Refresh
 - IFaxIncomingJob.Refresh
---

# IFaxIncomingJob::Refresh


## -description

The <b>Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_QUEUE</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-queue">Visual Basic Example</a>
