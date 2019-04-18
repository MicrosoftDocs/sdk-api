---
UID: NF:faxcomex.IFaxDocument.get_ScheduleType
title: IFaxDocument::get_ScheduleType (faxcomex.h)
author: windows-sdk-content
description: The IFaxDocument::get_ScheduleType property indicates when to schedule the fax job; for example, you can specify that the fax service send the fax immediately, at a specified time, or during a predefined discount period.
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_scheduletype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5jz9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDocument interface [Fax Service],ScheduleType property, IFaxDocument.ScheduleType, IFaxDocument.get_ScheduleType, IFaxDocument.put_ScheduleType, IFaxDocument::ScheduleType, IFaxDocument::get_ScheduleType, IFaxDocument::put_ScheduleType, ScheduleType property [Fax Service], ScheduleType property [Fax Service],IFaxDocument interface, _mfax_faxdocument.scheduletype, fax._mfax_faxdocument_cpp_mfax_faxdocument_scheduletype_cpp, fax._mfax_faxdocument_scheduletype, faxcomex/IFaxDocument::ScheduleType, faxcomex/IFaxDocument::get_ScheduleType, faxcomex/IFaxDocument::put_ScheduleType, get_ScheduleType
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
 - IFaxDocument.ScheduleType
 - IFaxDocument.get_ScheduleType
 - IFaxDocument.put_ScheduleType
 - IFaxDocument.get_ScheduleType
 - IFaxDocument.put_ScheduleType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDocument::get_ScheduleType


## -description


The <b>IFaxDocument::get_ScheduleType</b> property indicates when to schedule the fax job; for example, you can specify that the fax service send the fax immediately, at a specified time, or during a predefined discount period.

This property is read/write.


## -parameters


## -remarks



By default, <b>IFaxDocument::get_ScheduleType</b> is set to <a href="https://msdn.microsoft.com/en-us/library/ms689199(v=VS.85).aspx">fstNOW</a>, indicating that the fax will be sent as soon as the device is available.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685960(v=VS.85).aspx">IFaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692936(v=VS.85).aspx">Visual Basic Example</a>
 

 

