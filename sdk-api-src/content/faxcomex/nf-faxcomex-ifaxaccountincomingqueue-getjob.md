---
UID: NF:faxcomex.IFaxAccountIncomingQueue.GetJob
title: IFaxAccountIncomingQueue::GetJob (faxcomex.h)
description: Returns an incoming fax job in the job queue of the current fax account according to the job's ID.
helpviewer_keywords: ["GetJob","GetJob method [Fax Service]","GetJob method [Fax Service]","IFaxAccountIncomingQueue interface","IFaxAccountIncomingQueue interface [Fax Service]","GetJob method","IFaxAccountIncomingQueue.GetJob","IFaxAccountIncomingQueue::GetJob","_mfax_faxaccountincomingqueue.getjob","fax._mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjob_cpp","fax._mfax_faxaccountincomingqueue_getjob","faxcomex/IFaxAccountIncomingQueue::GetJob"]
old-location: fax\_mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingqueue\getjob.htm
ms.date: 12/05/2018
ms.keywords: GetJob, GetJob method [Fax Service], GetJob method [Fax Service],IFaxAccountIncomingQueue interface, IFaxAccountIncomingQueue interface [Fax Service],GetJob method, IFaxAccountIncomingQueue.GetJob, IFaxAccountIncomingQueue::GetJob, _mfax_faxaccountincomingqueue.getjob, fax._mfax_faxaccountincomingqueue_cpp_mfax_faxaccountincomingqueue_getjob_cpp, fax._mfax_faxaccountincomingqueue_getjob, faxcomex/IFaxAccountIncomingQueue::GetJob
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
 - IFaxAccountIncomingQueue::GetJob
 - faxcomex/IFaxAccountIncomingQueue::GetJob
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
 - IFaxAccountIncomingQueue.GetJob
 - IFaxAccountIncomingQueue.GetJob
---

# IFaxAccountIncomingQueue::GetJob


## -description

Returns an incoming fax job in the job queue of the current fax account according to the job's ID.

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

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_LOW</a> access rights.

If the setting "All incoming faxes are viewable by everyone" is true (see <a href="/previous-versions/windows/desktop/fax/-mfax-faxconfiguration-incomingfaxesarepublic-vb">IncomingFaxesArePublic</a>) or if the current user has <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_RECEIVE_FOLDER</a> access rights, then the set returned includes all the messages present in the fax server incoming queue.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingqueue">FaxAccountIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingqueue">IFaxAccountIncomingQueue</a>