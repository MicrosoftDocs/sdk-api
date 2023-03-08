---
UID: NF:faxcomex.IFaxIncomingQueue.GetJob
title: IFaxIncomingQueue::GetJob (faxcomex.h)
description: The GetJob method returns an incoming fax job in the job queue according to its ID.
helpviewer_keywords: ["GetJob","GetJob method [Fax Service]","GetJob method [Fax Service]","IFaxIncomingQueue interface","IFaxIncomingQueue interface [Fax Service]","GetJob method","IFaxIncomingQueue.GetJob","IFaxIncomingQueue::GetJob","_mfax_faxincomingqueue.getjob","fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjob_cpp","fax._mfax_faxincomingqueue_getjob","faxcomex/IFaxIncomingQueue::GetJob"]
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6crm.htm
ms.date: 12/05/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxIncomingQueue interface, IFaxIncomingQueue interface [Fax Service],GetJob method, IFaxIncomingQueue.GetJob, IFaxIncomingQueue::GetJob, _mfax_faxincomingqueue.getjob, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_getjob_cpp, fax._mfax_faxincomingqueue_getjob, faxcomex/IFaxIncomingQueue::GetJob
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
 - IFaxIncomingQueue::GetJob
 - faxcomex/IFaxIncomingQueue::GetJob
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
 - IFaxIncomingQueue.GetJob
 - IFaxIncomingQueue.GetJob
---

# IFaxIncomingQueue::GetJob


## -description

The <b>GetJob</b> method returns an incoming fax job in the job queue according to its ID.

## -parameters

### -param bstrJobId [in]

Type: <b>BSTR</b>

Specifies the job ID.

### -param pFaxIncomingJob [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_JOBS</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farSUBMIT_LOW</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>