---
UID: NF:faxcomex.IFaxOutgoingJob.get_TransmissionEnd
title: IFaxOutgoingJob::get_TransmissionEnd (faxcomex.h)
description: The IFaxOutgoingJob::get_TransmissionEnd property indicates the time that the outbound fax job completed transmission.
helpviewer_keywords: ["IFaxOutgoingJob interface [Fax Service]","TransmissionEnd property","IFaxOutgoingJob.TransmissionEnd","IFaxOutgoingJob.get_TransmissionEnd","IFaxOutgoingJob::TransmissionEnd","IFaxOutgoingJob::get_TransmissionEnd","TransmissionEnd property [Fax Service]","TransmissionEnd property [Fax Service]","IFaxOutgoingJob interface","_mfax_faxoutgoingjob.transmissionend","fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_transmissionend_cpp","fax._mfax_faxoutgoingjob_transmissionend","faxcomex/IFaxOutgoingJob::TransmissionEnd","faxcomex/IFaxOutgoingJob::get_TransmissionEnd","get_TransmissionEnd"]
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_transmissionend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_50x0.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob interface [Fax Service],TransmissionEnd property, IFaxOutgoingJob.TransmissionEnd, IFaxOutgoingJob.get_TransmissionEnd, IFaxOutgoingJob::TransmissionEnd, IFaxOutgoingJob::get_TransmissionEnd, TransmissionEnd property [Fax Service], TransmissionEnd property [Fax Service],IFaxOutgoingJob interface, _mfax_faxoutgoingjob.transmissionend, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_transmissionend_cpp, fax._mfax_faxoutgoingjob_transmissionend, faxcomex/IFaxOutgoingJob::TransmissionEnd, faxcomex/IFaxOutgoingJob::get_TransmissionEnd, get_TransmissionEnd
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
 - IFaxOutgoingJob::get_TransmissionEnd
 - faxcomex/IFaxOutgoingJob::get_TransmissionEnd
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
 - IFaxOutgoingJob.TransmissionEnd
 - IFaxOutgoingJob.get_TransmissionEnd
 - IFaxOutgoingJob.get_TransmissionEnd
---

# IFaxOutgoingJob::get_TransmissionEnd


## -description

The <b>IFaxOutgoingJob::get_TransmissionEnd</b> property indicates the time that the outbound fax job completed transmission.

This property is read-only.

## -parameters

## -remarks

The property is not valid as long as the fax is still being sent by the fax device. It will have a value only after the transmission has ended. In the case of an individual fax, once the transmission has ended, the fax will be moved to the outgoing archive, and you will not be able to retrieve this value. You can instead retrieve the value of the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-transmissionend-vb">TransmissionEnd</a> property. In the case of a broadcast, each fax of the broadcast remains in the outgoing queue until the entire broadcast has been completed, and you can retrieve the value for the <b>IFaxOutgoingJob::get_TransmissionEnd</b> property.

In the case of a failed fax, this property will be assigned a value of zero. If you try to retrieve the property for a failed fax, you will receive an error.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>