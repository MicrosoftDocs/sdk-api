---
UID: NF:faxcomex.IFaxIncomingQueue.GetJobs
title: IFaxIncomingQueue::GetJobs (faxcomex.h)
description: The GetJobs method returns the collection of inbound fax jobs in the queue.
helpviewer_keywords: ["GetJobs","GetJobs method [Fax Service]","GetJobs method [Fax Service]","IFaxIncomingQueue interface","IFaxIncomingQueue interface [Fax Service]","GetJobs method","IFaxIncomingQueue.GetJobs","IFaxIncomingQueue::GetJobs","_mfax_faxincomingqueue.getjobs","fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp","fax._mfax_faxincomingqueue_getjobs","faxcomex/IFaxIncomingQueue::GetJobs"]
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6p6b.htm
ms.date: 12/05/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxIncomingQueue interface, IFaxIncomingQueue interface [Fax Service],GetJobs method, IFaxIncomingQueue.GetJobs, IFaxIncomingQueue::GetJobs, _mfax_faxincomingqueue.getjobs, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjobs_cpp, fax._mfax_faxincomingqueue_getjobs, faxcomex/IFaxIncomingQueue::GetJobs
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
 - IFaxIncomingQueue::GetJobs
 - faxcomex/IFaxIncomingQueue::GetJobs
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
 - IFaxIncomingQueue.GetJobs
 - IFaxIncomingQueue.GetJobs
---

# IFaxIncomingQueue::GetJobs


## -description

The <b>GetJobs</b> method returns the collection of inbound fax jobs in the queue.

## -parameters

### -param pFaxIncomingJobs [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-queue">Visual Basic Example</a>