---
UID: NF:faxcomex.IFaxJobStatus.get_TransmissionEnd
title: IFaxJobStatus::get_TransmissionEnd (faxcomex.h)
description: The TransmissionEnd property indicates the time that the fax job completed transmission.
helpviewer_keywords: ["IFaxJobStatus interface [Fax Service]","TransmissionEnd property","IFaxJobStatus.TransmissionEnd","IFaxJobStatus.get_TransmissionEnd","IFaxJobStatus::TransmissionEnd","IFaxJobStatus::get_TransmissionEnd","TransmissionEnd property [Fax Service]","TransmissionEnd property [Fax Service]","IFaxJobStatus interface","_mfax_faxjobstatus.transmissionend","fax._mfax_faxjobstatus_cpp_mfax_faxjobstatus_transmissionend_cpp","fax._mfax_faxjobstatus_transmissionend","faxcomex/IFaxJobStatus::TransmissionEnd","faxcomex/IFaxJobStatus::get_TransmissionEnd","get_TransmissionEnd"]
old-location: fax\_mfax_faxjobstatus_cpp_mfax_faxjobstatus_transmissionend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7fxg.htm
ms.date: 12/05/2018
ms.keywords: IFaxJobStatus interface [Fax Service],TransmissionEnd property, IFaxJobStatus.TransmissionEnd, IFaxJobStatus.get_TransmissionEnd, IFaxJobStatus::TransmissionEnd, IFaxJobStatus::get_TransmissionEnd, TransmissionEnd property [Fax Service], TransmissionEnd property [Fax Service],IFaxJobStatus interface, _mfax_faxjobstatus.transmissionend, fax._mfax_faxjobstatus_cpp_mfax_faxjobstatus_transmissionend_cpp, fax._mfax_faxjobstatus_transmissionend, faxcomex/IFaxJobStatus::TransmissionEnd, faxcomex/IFaxJobStatus::get_TransmissionEnd, get_TransmissionEnd
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
 - IFaxJobStatus::get_TransmissionEnd
 - faxcomex/IFaxJobStatus::get_TransmissionEnd
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
 - IFaxJobStatus.TransmissionEnd
 - IFaxJobStatus.get_TransmissionEnd
 - IFaxJobStatus.get_TransmissionEnd
---

# IFaxJobStatus::get_TransmissionEnd


## -description

The <b>TransmissionEnd</b> property indicates the time that the fax job completed transmission.

This property is read-only.

## -parameters

## -remarks

The property is not valid as long as the fax is still being received by the fax device.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus">FaxJobStatus</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxjobstatus">IFaxJobStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Visual Basic Example</a>