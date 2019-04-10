---
UID: NF:faxcomex.IFaxOutgoingJob.get_TransmissionStart
title: IFaxOutgoingJob::get_TransmissionStart (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingJob::get_TransmissionStart property indicates the time that the fax outbound job began transmitting. This property will have a value only after the transmission has started.
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_transmissionstart_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_27w4.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob interface [Fax Service],TransmissionStart property, IFaxOutgoingJob.TransmissionStart, IFaxOutgoingJob.get_TransmissionStart, IFaxOutgoingJob::TransmissionStart, IFaxOutgoingJob::get_TransmissionStart, TransmissionStart property [Fax Service], TransmissionStart property [Fax Service],IFaxOutgoingJob interface, _mfax_faxoutgoingjob.transmissionstart, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_transmissionstart_cpp, fax._mfax_faxoutgoingjob_transmissionstart, faxcomex/IFaxOutgoingJob::TransmissionStart, faxcomex/IFaxOutgoingJob::get_TransmissionStart, get_TransmissionStart
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJob.TransmissionStart
 - IFaxOutgoingJob.get_TransmissionStart
 - IFaxOutgoingJob.get_TransmissionStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingJob::get_TransmissionStart


## -description


The <b>IFaxOutgoingJob::get_TransmissionStart</b> property indicates the time that the fax outbound job began transmitting. This property will have a value only after the transmission has started.

This property is read-only.


## -parameters


## -remarks



In the case of a failed fax, this property will be assigned a value of zero. If you try to retrieve the property for a failed fax, you will receive an error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689116(v=VS.85).aspx">IFaxOutgoingJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693393(v=VS.85).aspx">Visual Basic Example</a>
 

 

