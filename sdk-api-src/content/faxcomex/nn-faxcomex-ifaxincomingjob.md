---
UID: NN:faxcomex.IFaxIncomingJob
title: IFaxIncomingJob (faxcomex.h)
description: The IFaxIncomingJob interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue.
helpviewer_keywords: ["IFaxIncomingJob","IFaxIncomingJob interface [Fax Service]","IFaxIncomingJob interface [Fax Service]","described","_mfax_faxincomingjob_cpp","fax._mfax_faxincomingjob_cpp","faxcomex/IFaxIncomingJob"]
old-location: fax\_mfax_faxincomingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1r4y_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob, IFaxIncomingJob interface [Fax Service], IFaxIncomingJob interface [Fax Service],described, _mfax_faxincomingjob_cpp, fax._mfax_faxincomingjob_cpp, faxcomex/IFaxIncomingJob
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
 - IFaxIncomingJob
 - faxcomex/IFaxIncomingJob
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
 - IFaxIncomingJob
---

# IFaxIncomingJob interface


## -description

The <b>IFaxIncomingJob</b> interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue. The interface also includes methods to cancel an incoming fax job and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an inbound fax job to a file on the local computer.

The <b>IFaxIncomingJob</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a> interface.

## -inheritance

The <b>IFaxIncomingJob</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingJob</b> also has these types of members:

## -remarks

To create a <b>FaxIncomingJob</b> object in C++, call the <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjobs-get_item">IFaxIncomingJobs::get_Item</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a>
