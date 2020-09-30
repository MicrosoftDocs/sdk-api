---
UID: NN:faxcomex.IFaxOutgoingJob2
title: IFaxOutgoingJob2 (faxcomex.h)
description: Describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue.
helpviewer_keywords: ["IFaxOutgoingJob2","IFaxOutgoingJob2 interface [Fax Service]","IFaxOutgoingJob2 interface [Fax Service]","described","_mfax_faxoutgoingjob2_cpp","fax._mfax_faxoutgoingjob2_cpp","faxcomex/IFaxOutgoingJob2"]
old-location: fax\_mfax_faxoutgoingjob2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingjob2\faxinto_z_ifaxoutgoingjob2.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob2, IFaxOutgoingJob2 interface [Fax Service], IFaxOutgoingJob2 interface [Fax Service],described, _mfax_faxoutgoingjob2_cpp, fax._mfax_faxoutgoingjob2_cpp, faxcomex/IFaxOutgoingJob2
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
 - IFaxOutgoingJob2
 - faxcomex/IFaxOutgoingJob2
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
 - IFaxOutgoingJob2
---

# IFaxOutgoingJob2 interface


## -description

Describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue. It inherits all the functionality of the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a> interface. Additionally, it provides new read-only properties to indicate whether the outgoing fax has a cover page, the schedule type of the fax, and the address of its recipient.



<div class="alert"><b>Note</b>  This interface is supported only on Windows Vista and later.</div><div> </div>

## -remarks

A default implementation of <b>IFaxOutgoingJob2</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a> object. On Windows XP and earlier, the <b>FaxOutgoingJob</b> object implements <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>.