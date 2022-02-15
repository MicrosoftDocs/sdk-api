---
UID: NF:faxcomex.IFaxOutgoingJob.Refresh
title: IFaxOutgoingJob::Refresh (faxcomex.h)
description: The Refresh method refreshes FaxOutgoingJob object information from the fax server.
helpviewer_keywords: ["IFaxOutgoingJob interface [Fax Service]","Refresh method","IFaxOutgoingJob.Refresh","IFaxOutgoingJob::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxOutgoingJob interface","_mfax_faxoutgoingjob.refresh","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_refresh_cpp","fax._mfax_faxoutgoingjob_refresh","faxcomex/IFaxOutgoingJob::Refresh"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_2oq0.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob interface [Fax Service],Refresh method, IFaxOutgoingJob.Refresh, IFaxOutgoingJob::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingJob interface, _mfax_faxoutgoingjob.refresh, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_refresh_cpp, fax._mfax_faxoutgoingjob_refresh, faxcomex/IFaxOutgoingJob::Refresh
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
 - IFaxOutgoingJob::Refresh
 - faxcomex/IFaxOutgoingJob::Refresh
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
 - IFaxOutgoingJob.Refresh
 - IFaxOutgoingJob.Refresh
---

# IFaxOutgoingJob::Refresh


## -description

The Refresh method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a> object information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <b>farQUERY_JOBS</b> access right.

With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farQUERY_JOBS</b> access right, users will be able to use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>
