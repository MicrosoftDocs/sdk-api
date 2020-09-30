---
UID: NN:faxcomex.IFaxJobStatus
title: IFaxJobStatus (faxcomex.h)
description: The IFaxJobStatus interface is used for notifications and to hold the dynamic information of the job.
helpviewer_keywords: ["IFaxJobStatus","IFaxJobStatus interface [Fax Service]","IFaxJobStatus interface [Fax Service]","described","_mfax_faxjobstatus_cpp","fax._mfax_faxjobstatus_cpp","faxcomex/IFaxJobStatus"]
old-location: fax\_mfax_faxjobstatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3p6b_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxJobStatus, IFaxJobStatus interface [Fax Service], IFaxJobStatus interface [Fax Service],described, _mfax_faxjobstatus_cpp, fax._mfax_faxjobstatus_cpp, faxcomex/IFaxJobStatus
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
 - IFaxJobStatus
 - faxcomex/IFaxJobStatus
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
 - IFaxJobStatus
---

# IFaxJobStatus interface


## -description

The <b>IFaxJobStatus</b> interface is used for notifications and to hold the dynamic information of the job. Dynamic information is data that changes as a job progresses. This may include the current job status, the page that is currently being transmitted, and the number of attempts the fax service has made to transmit the job (retries). The fax service uses this object to notify a fax client application of job updates. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-job-status">Fax Job Status</a>.

## -remarks

You do not create the <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus">FaxJobStatus</a> object. It is received as part of a notification when you implement <a href="/windows/win32/api/faxcomex/nf-faxcomex-_ifaxaccountnotify-onincomingjobchanged">IFaxServerNotify::OnIncomingJobChanged</a> or <a href="https://msdn.microsoft.com/132747ed-04b4-4803-976c-5274d8c9f73d">IFaxServerNotify::OnOutgoingJobChanged</a>, which include a parameter of the type <b>FaxJobStatus</b>. When the event occurs and the implemented function is called, you receive this object containing the dynamic information.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus">FaxJobStatus</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>