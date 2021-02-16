---
UID: NF:faxcomex.IFaxIncomingJob.get_TransmissionEnd
title: IFaxIncomingJob::get_TransmissionEnd (faxcomex.h)
description: The TransmissionEnd property indicates the time at which the inbound fax job completed transmission.
helpviewer_keywords: ["IFaxIncomingJob interface [Fax Service]","TransmissionEnd property","IFaxIncomingJob.TransmissionEnd","IFaxIncomingJob.get_TransmissionEnd","IFaxIncomingJob::TransmissionEnd","IFaxIncomingJob::get_TransmissionEnd","TransmissionEnd property [Fax Service]","TransmissionEnd property [Fax Service]","IFaxIncomingJob interface","_mfax_faxincomingjob.transmissionend","fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_transmissionend_cpp","fax._mfax_faxincomingjob_transmissionend","faxcomex/IFaxIncomingJob::TransmissionEnd","faxcomex/IFaxIncomingJob::get_TransmissionEnd","get_TransmissionEnd"]
old-location: fax\_mfax_faxincomingjob_cpp_mfax_faxincomingjob_transmissionend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4quc.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],TransmissionEnd property, IFaxIncomingJob.TransmissionEnd, IFaxIncomingJob.get_TransmissionEnd, IFaxIncomingJob::TransmissionEnd, IFaxIncomingJob::get_TransmissionEnd, TransmissionEnd property [Fax Service], TransmissionEnd property [Fax Service],IFaxIncomingJob interface, _mfax_faxincomingjob.transmissionend, fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_transmissionend_cpp, fax._mfax_faxincomingjob_transmissionend, faxcomex/IFaxIncomingJob::TransmissionEnd, faxcomex/IFaxIncomingJob::get_TransmissionEnd, get_TransmissionEnd
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
 - IFaxIncomingJob::get_TransmissionEnd
 - faxcomex/IFaxIncomingJob::get_TransmissionEnd
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
 - IFaxIncomingJob.TransmissionEnd
 - IFaxIncomingJob.get_TransmissionEnd
 - IFaxIncomingJob.get_TransmissionEnd
---

# IFaxIncomingJob::get_TransmissionEnd


## -description

The <b>TransmissionEnd</b> property indicates the time at which the inbound fax job completed transmission.

This property is read-only.

## -parameters

## -remarks

The <b>TransmissionEnd</b> property is not valid as long as the fax is still being received by the fax device. In the case of a fax that is still in progress, this property will be assigned a value of zero. If you try to retrieve the property for a fax that is still in progress you will receive an error.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-queue">Visual Basic Example</a>