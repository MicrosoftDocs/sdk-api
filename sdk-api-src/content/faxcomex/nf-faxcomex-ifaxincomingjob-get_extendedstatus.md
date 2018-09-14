---
UID: NF:faxcomex.IFaxIncomingJob.get_ExtendedStatus
title: IFaxIncomingJob::get_ExtendedStatus
author: windows-sdk-content
description: The ExtendedStatus property is a null-terminated string that describes the job's extended status.
old-location: fax\_mfax_faxincomingjob_cpp_mfax_faxincomingjob_extendedstatus_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7v03.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ExtendedStatus property [Fax Service], ExtendedStatus property [Fax Service],IFaxIncomingJob interface, IFaxIncomingJob interface [Fax Service],ExtendedStatus property, IFaxIncomingJob.ExtendedStatus, IFaxIncomingJob.get_ExtendedStatus, IFaxIncomingJob::ExtendedStatus, IFaxIncomingJob::get_ExtendedStatus, _mfax_faxincomingjob.extendedstatus, fax._mfax_faxincomingjob_cpp_mfax_faxincomingjob_extendedstatus_cpp, fax._mfax_faxincomingjob_extendedstatus, faxcomex/IFaxIncomingJob::ExtendedStatus, faxcomex/IFaxIncomingJob::get_ExtendedStatus, get_ExtendedStatus
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
 - IFaxIncomingJob.ExtendedStatus
 - IFaxIncomingJob.get_ExtendedStatus
 - IFaxIncomingJob.get_ExtendedStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJob::get_ExtendedStatus


## -description


The <b>ExtendedStatus</b> property is a null-terminated string that describes the job's extended status.

This property is read-only.


## -parameters


## -remarks



The <b>ExtendedStatus</b> property can have a value only if the fax service provider (FSP) returns a proprietary status code in the <a href="https://msdn.microsoft.com/15333cd3-e71a-451c-ae93-9e217ea0895c">ExtendedStatusCode</a> property. Otherwise, the <b>ExtendedStatus</b> property will contain an empty string.




## -see-also




<a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/88cde2d4-09ee-4fbf-8a75-35de58dd45f5">Visual Basic Example</a>
 

 

