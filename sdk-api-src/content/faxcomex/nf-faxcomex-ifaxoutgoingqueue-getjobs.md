---
UID: NF:faxcomex.IFaxOutgoingQueue.GetJobs
title: IFaxOutgoingQueue::GetJobs (faxcomex.h)
description: The IFaxOutgoingQueue::GetJobs method returns a collection of the outbound fax jobs in the job queue.
helpviewer_keywords: ["GetJobs","GetJobs method [Fax Service]","GetJobs method [Fax Service]","IFaxOutgoingQueue interface","IFaxOutgoingQueue interface [Fax Service]","GetJobs method","IFaxOutgoingQueue.GetJobs","IFaxOutgoingQueue::GetJobs","_mfax_faxoutgoingqueue.getjobs","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_getjobs_cpp","fax._mfax_faxoutgoingqueue_getjobs","faxcomex/IFaxOutgoingQueue::GetJobs"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_978z.htm
ms.date: 12/05/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],GetJobs method, IFaxOutgoingQueue.GetJobs, IFaxOutgoingQueue::GetJobs, _mfax_faxoutgoingqueue.getjobs, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_getjobs_cpp, fax._mfax_faxoutgoingqueue_getjobs, faxcomex/IFaxOutgoingQueue::GetJobs
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
 - IFaxOutgoingQueue::GetJobs
 - faxcomex/IFaxOutgoingQueue::GetJobs
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
 - IFaxOutgoingQueue.GetJobs
 - IFaxOutgoingQueue.GetJobs
---

# IFaxOutgoingQueue::GetJobs


## -description

The <b>IFaxOutgoingQueue::GetJobs</b> method returns a collection of the outbound fax jobs in the job queue.

## -parameters

### -param pFaxOutgoingJobs [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs">FaxOutgoingJobs</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs">FaxOutgoingJobs</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> or <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> access right.

With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access right, users can use this method only for their own faxes. With the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> access right, users can use this method for all faxes on the server.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Managing Outgoing Jobs</a>