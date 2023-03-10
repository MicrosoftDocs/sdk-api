---
UID: NN:faxcomex.IFaxOutgoingJob
title: IFaxOutgoingJob (faxcomex.h)
description: The IFaxOutgoingJob interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue.
helpviewer_keywords: ["IFaxOutgoingJob","IFaxOutgoingJob interface [Fax Service]","IFaxOutgoingJob interface [Fax Service]","described","_mfax_faxoutgoingjob_cpp","fax._mfax_faxoutgoingjob_cpp","faxcomex/IFaxOutgoingJob"]
old-location: fax\_mfax_faxoutgoingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4mjm_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob, IFaxOutgoingJob interface [Fax Service], IFaxOutgoingJob interface [Fax Service],described, _mfax_faxoutgoingjob_cpp, fax._mfax_faxoutgoingjob_cpp, faxcomex/IFaxOutgoingJob
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
 - IFaxOutgoingJob
 - faxcomex/IFaxOutgoingJob
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
 - IFaxOutgoingJob
---

# IFaxOutgoingJob interface


## -description

The <b>IFaxOutgoingJob</b> interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue. The object also includes methods to cancel, pause, resume, or restart an outgoing fax job, and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an outbound fax job, to a file on the local computer.

## -inheritance

The <b>IFaxOutgoingJob</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingJob</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxOutgoingJob</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a> object.
