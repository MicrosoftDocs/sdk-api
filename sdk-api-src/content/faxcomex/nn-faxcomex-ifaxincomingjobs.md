---
UID: NN:faxcomex.IFaxIncomingJobs
title: IFaxIncomingJobs (faxcomex.h)
description: The IFaxIncomingJobs interface is used by a fax client application to manage the inbound fax jobs in a fax server's job queue. Each incoming job is represented by a FaxIncomingJob object.
helpviewer_keywords: ["IFaxIncomingJobs","IFaxIncomingJobs interface [Fax Service]","IFaxIncomingJobs interface [Fax Service]","described","_mfax_faxincomingjobs_cpp","fax._mfax_faxincomingjobs_cpp","faxcomex/IFaxIncomingJobs"]
old-location: fax\_mfax_faxincomingjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_28vn_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJobs, IFaxIncomingJobs interface [Fax Service], IFaxIncomingJobs interface [Fax Service],described, _mfax_faxincomingjobs_cpp, fax._mfax_faxincomingjobs_cpp, faxcomex/IFaxIncomingJobs
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
 - IFaxIncomingJobs
 - faxcomex/IFaxIncomingJobs
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
 - IFaxIncomingJobs
---

# IFaxIncomingJobs interface


## -description

The <b>IFaxIncomingJobs</b> interface is used by a fax client application to manage the inbound fax jobs in a fax server's job queue. Each incoming job is represented by a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object.

The <b>IFaxIncomingJobs</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a> interface.

## -inheritance

The <b>IFaxIncomingJobs</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingJobs</b> also has these types of members:

## -remarks

To create a <b>FaxIncomingJobs</b> object in C++, call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue-getjobs-vb">IFaxIncomingQueue::GetJobs</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>
