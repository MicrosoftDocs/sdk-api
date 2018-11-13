---
UID: NF:faxcomex.IFaxDocument.put_ScheduleTime
title: IFaxDocument::put_ScheduleTime
author: windows-sdk-content
description: The IFaxDocument::get_ScheduleTime property indicates the time to submit the fax for processing to the fax service.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_scheduletime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_459h.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxDocument interface [Fax Service],ScheduleTime property, IFaxDocument.ScheduleTime, IFaxDocument.get_ScheduleTime, IFaxDocument.put_ScheduleTime, IFaxDocument::ScheduleTime, IFaxDocument::get_ScheduleTime, IFaxDocument::put_ScheduleTime, ScheduleTime property [Fax Service], ScheduleTime property [Fax Service],IFaxDocument interface, _mfax_faxdocument.scheduletime, fax._mfax_faxdocument_cpp_mfax_faxdocument_scheduletime_cpp, fax._mfax_faxdocument_scheduletime, faxcomex/IFaxDocument::ScheduleTime, faxcomex/IFaxDocument::get_ScheduleTime, faxcomex/IFaxDocument::put_ScheduleTime, put_ScheduleTime
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
 - IFaxDocument.ScheduleTime
 - IFaxDocument.get_ScheduleTime
 - IFaxDocument.put_ScheduleTime
 - IFaxDocument.get_ScheduleTime
 - IFaxDocument.put_ScheduleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument::put_ScheduleTime


## -description


The <b>IFaxDocument::get_ScheduleTime</b> property indicates the time to submit the fax for processing to the fax service.

This property is read/write.


## -parameters


## -remarks



If the time specified has passed, the fax service sends the fax as soon as a device is available. By default, <b>IFaxDocument::get_ScheduleTime</b> is set to zero, meaning that no time is specified.

Note that the fax service ignores this parameter unless you set the <a href="https://msdn.microsoft.com/cbcfcdb1-de89-4e74-8f69-b25d4813f28d">IFaxDocument::get_ScheduleType</a> property to <a href="https://msdn.microsoft.com/a93dca50-f5ef-4bf0-b773-5d00929be543">fstSpecific_TIME</a>.

<div class="alert"><b>Note</b>  The value of the <b>IFaxDocument::get_ScheduleTime</b> property must include the date and time for submitting the fax.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a87e6de7-1541-4f9e-b411-d8c6907bf93e">FaxDocument</a>



<a href="https://msdn.microsoft.com/926f01ab-66a7-49c8-95cf-7f80925401be">IFaxDocument</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

