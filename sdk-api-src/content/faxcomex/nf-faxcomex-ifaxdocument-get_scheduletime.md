---
UID: NF:faxcomex.IFaxDocument.get_ScheduleTime
title: IFaxDocument::get_ScheduleTime (faxcomex.h)
description: The IFaxDocument::get_ScheduleTime property indicates the time to submit the fax for processing to the fax service. (Get)
helpviewer_keywords: ["IFaxDocument interface [Fax Service]","ScheduleTime property","IFaxDocument.ScheduleTime","IFaxDocument.get_ScheduleTime","IFaxDocument.put_ScheduleTime","IFaxDocument::ScheduleTime","IFaxDocument::get_ScheduleTime","IFaxDocument::put_ScheduleTime","ScheduleTime property [Fax Service]","ScheduleTime property [Fax Service]","IFaxDocument interface","_mfax_faxdocument.scheduletime","fax._mfax_faxdocument_cpp_mfax_faxdocument_scheduletime_cpp","fax._mfax_faxdocument_scheduletime","faxcomex/IFaxDocument::ScheduleTime","faxcomex/IFaxDocument::get_ScheduleTime","faxcomex/IFaxDocument::put_ScheduleTime","get_ScheduleTime"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_scheduletime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_459h.htm
ms.date: 12/05/2018
ms.keywords: IFaxDocument interface [Fax Service],ScheduleTime property, IFaxDocument.ScheduleTime, IFaxDocument.get_ScheduleTime, IFaxDocument.put_ScheduleTime, IFaxDocument::ScheduleTime, IFaxDocument::get_ScheduleTime, IFaxDocument::put_ScheduleTime, ScheduleTime property [Fax Service], ScheduleTime property [Fax Service],IFaxDocument interface, _mfax_faxdocument.scheduletime, fax._mfax_faxdocument_cpp_mfax_faxdocument_scheduletime_cpp, fax._mfax_faxdocument_scheduletime, faxcomex/IFaxDocument::ScheduleTime, faxcomex/IFaxDocument::get_ScheduleTime, faxcomex/IFaxDocument::put_ScheduleTime, get_ScheduleTime
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
 - IFaxDocument::get_ScheduleTime
 - faxcomex/IFaxDocument::get_ScheduleTime
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
 - IFaxDocument.ScheduleTime
 - IFaxDocument.get_ScheduleTime
 - IFaxDocument.put_ScheduleTime
 - IFaxDocument.get_ScheduleTime
 - IFaxDocument.put_ScheduleTime
---

# IFaxDocument::get_ScheduleTime


## -description

The <b>IFaxDocument::get_ScheduleTime</b> property indicates the time to submit the fax for processing to the fax service.

This property is read/write.

## -parameters

## -remarks

If the time specified has passed, the fax service sends the fax as soon as a device is available. By default, <b>IFaxDocument::get_ScheduleTime</b> is set to zero, meaning that no time is specified.

Note that the fax service ignores this parameter unless you set the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-scheduletype-vb">IFaxDocument::get_ScheduleType</a> property to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_schedule_type_enum">fstSpecific_TIME</a>.

<div class="alert"><b>Note</b>  The value of the <b>IFaxDocument::get_ScheduleTime</b> property must include the date and time for submitting the fax.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
