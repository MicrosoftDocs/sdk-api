---
UID: NF:faxcomex.IFaxIncomingJob.get_TransmissionEnd
title: IFaxIncomingJob::get_TransmissionEnd
author: windows-sdk-content
description: The TransmissionEnd property indicates the time at which the inbound fax job completed transmission.
old-location: fax\_mfax_faxincomingjob_cpp_mfax_faxincomingjob_transmissionend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4quc.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxIncomingJob interface [Fax Service],TransmissionEnd property, IFaxIncomingJob.TransmissionEnd, IFaxIncomingJob.get_TransmissionEnd, IFaxIncomingJob::TransmissionEnd, IFaxIncomingJob::get_TransmissionEnd, TransmissionEnd property [Fax Service], TransmissionEnd property [Fax Service],IFaxIncomingJob interface, _mfax_faxincomingjob.transmissionend, fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_transmissionend_cpp, fax._mfax_faxincomingjob_transmissionend, faxcomex/IFaxIncomingJob::TransmissionEnd, faxcomex/IFaxIncomingJob::get_TransmissionEnd, get_TransmissionEnd
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFaxIncomingJob.TransmissionEnd
 - IFaxIncomingJob.get_TransmissionEnd
 - IFaxIncomingJob.get_TransmissionEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJob::get_TransmissionEnd


## -description


The <b>TransmissionEnd</b> property indicates the time at which the inbound fax job completed transmission.

This property is read-only.


## -parameters


## -remarks



The <b>TransmissionEnd</b> property is not valid as long as the fax is still being received by the fax device. In the case of a fax that is still in progress, this property will be assigned a value of zero. If you try to retrieve the property for a fax that is still in progress you will receive an error.




## -see-also




<a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/88cde2d4-09ee-4fbf-8a75-35de58dd45f5">Visual Basic Example</a>
 

 

