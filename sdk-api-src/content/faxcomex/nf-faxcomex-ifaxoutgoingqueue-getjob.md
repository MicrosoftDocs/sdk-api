---
UID: NF:faxcomex.IFaxOutgoingQueue.GetJob
title: IFaxOutgoingQueue::GetJob (faxcomex.h)
description: The IFaxOutgoingQueue::GetJob method returns an outbound fax job in the job queue according to its ID.
helpviewer_keywords: ["GetJob","GetJob method [Fax Service]","GetJob method [Fax Service]","IFaxOutgoingQueue interface","IFaxOutgoingQueue interface [Fax Service]","GetJob method","IFaxOutgoingQueue.GetJob","IFaxOutgoingQueue::GetJob","_mfax_faxoutgoingqueue.getjob_cpp","fax._mfax_faxoutgoingqueue_getjob_cpp","faxcomex/IFaxOutgoingQueue::GetJob"]
old-location: fax\_mfax_faxoutgoingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_3w6a_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],GetJob method, IFaxOutgoingQueue.GetJob, IFaxOutgoingQueue::GetJob, _mfax_faxoutgoingqueue.getjob_cpp, fax._mfax_faxoutgoingqueue_getjob_cpp, faxcomex/IFaxOutgoingQueue::GetJob
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
 - IFaxOutgoingQueue::GetJob
 - faxcomex/IFaxOutgoingQueue::GetJob
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
 - IFaxOutgoingQueue.GetJob
---

# IFaxOutgoingQueue::GetJob


## -description

The <b>IFaxOutgoingQueue::GetJob</b> method returns an outbound fax job in the job queue according to its ID.

## -parameters

### -param bstrJobId [in]

Type: <b>BSTR</b>

Specifies the job ID.

### -param pFaxOutgoingJob [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>**</b>

The address of a pointer that receives a <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> access right.

With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access right, users can use this method only for their own faxes. With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> access right, users can use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>