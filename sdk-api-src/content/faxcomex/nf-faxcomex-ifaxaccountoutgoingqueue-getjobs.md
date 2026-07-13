---
UID: NF:faxcomex.IFaxAccountOutgoingQueue.GetJobs
title: IFaxAccountOutgoingQueue::GetJobs (faxcomex.h)
description: Returns the collection of outbound fax jobs in the queue for the current fax account.
helpviewer_keywords: ["GetJobs","GetJobs method [Fax Service]","GetJobs method [Fax Service]","IFaxAccountOutgoingQueue interface","IFaxAccountOutgoingQueue interface [Fax Service]","GetJobs method","IFaxAccountOutgoingQueue.GetJobs","IFaxAccountOutgoingQueue::GetJobs","_mfax_faxaccountoutgoingqueue.getjobs","fax._mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp","fax._mfax_faxaccountoutgoingqueue_getjobs","faxcomex/IFaxAccountOutgoingQueue::GetJobs"]
old-location: fax\_mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingqueue\getjobs.htm
ms.date: 12/05/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxAccountOutgoingQueue interface, IFaxAccountOutgoingQueue interface [Fax Service],GetJobs method, IFaxAccountOutgoingQueue.GetJobs, IFaxAccountOutgoingQueue::GetJobs, _mfax_faxaccountoutgoingqueue.getjobs, fax._mfax_faxaccountoutgoingqueue_cpp_mfax_faxaccountoutgoingqueue_getjobs_cpp, fax._mfax_faxaccountoutgoingqueue_getjobs, faxcomex/IFaxAccountOutgoingQueue::GetJobs
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccountOutgoingQueue::GetJobs
 - faxcomex/IFaxAccountOutgoingQueue::GetJobs
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
 - IFaxAccountOutgoingQueue.GetJobs
 - IFaxAccountOutgoingQueue.GetJobs
---

# IFaxAccountOutgoingQueue::GetJobs


## -description

Returns the collection of outbound fax jobs in the queue for the current fax account.

## -parameters

### -param pFaxOutgoingJobs [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjobs">IFaxOutgoingJobs</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs">FaxOutgoingJobs</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingqueue">FaxAccountOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingqueue">IFaxAccountOutgoingQueue</a>