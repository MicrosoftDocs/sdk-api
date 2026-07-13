---
UID: NF:faxcomex.IFaxDocument.put_ScheduleType
title: IFaxDocument::put_ScheduleType (faxcomex.h)
description: The IFaxDocument::get_ScheduleType property indicates when to schedule the fax job; for example, you can specify that the fax service send the fax immediately, at a specified time, or during a predefined discount period. (Put)
helpviewer_keywords: ["IFaxDocument interface [Fax Service]","ScheduleType property","IFaxDocument.ScheduleType","IFaxDocument.get_ScheduleType","IFaxDocument.put_ScheduleType","IFaxDocument::ScheduleType","IFaxDocument::get_ScheduleType","IFaxDocument::put_ScheduleType","ScheduleType property [Fax Service]","ScheduleType property [Fax Service]","IFaxDocument interface","_mfax_faxdocument.scheduletype","fax._mfax_faxdocument_cpp_mfax_faxdocument_scheduletype_cpp","fax._mfax_faxdocument_scheduletype","faxcomex/IFaxDocument::ScheduleType","faxcomex/IFaxDocument::get_ScheduleType","faxcomex/IFaxDocument::put_ScheduleType","put_ScheduleType"]
old-location: fax\_mfax_faxdocument_cpp_mfax_faxdocument_scheduletype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5jz9.htm
ms.date: 12/05/2018
ms.keywords: IFaxDocument interface [Fax Service],ScheduleType property, IFaxDocument.ScheduleType, IFaxDocument.get_ScheduleType, IFaxDocument.put_ScheduleType, IFaxDocument::ScheduleType, IFaxDocument::get_ScheduleType, IFaxDocument::put_ScheduleType, ScheduleType property [Fax Service], ScheduleType property [Fax Service],IFaxDocument interface, _mfax_faxdocument.scheduletype, fax._mfax_faxdocument_cpp_mfax_faxdocument_scheduletype_cpp, fax._mfax_faxdocument_scheduletype, faxcomex/IFaxDocument::ScheduleType, faxcomex/IFaxDocument::get_ScheduleType, faxcomex/IFaxDocument::put_ScheduleType, put_ScheduleType
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
 - IFaxDocument::put_ScheduleType
 - faxcomex/IFaxDocument::put_ScheduleType
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
 - IFaxDocument.ScheduleType
 - IFaxDocument.get_ScheduleType
 - IFaxDocument.put_ScheduleType
 - IFaxDocument.get_ScheduleType
 - IFaxDocument.put_ScheduleType
---

# IFaxDocument::put_ScheduleType


## -description

The <b>IFaxDocument::get_ScheduleType</b> property indicates when to schedule the fax job; for example, you can specify that the fax service send the fax immediately, at a specified time, or during a predefined discount period.

This property is read/write.

## -parameters

## -remarks

By default, <b>IFaxDocument::get_ScheduleType</b> is set to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_schedule_type_enum">fstNOW</a>, indicating that the fax will be sent as soon as the device is available.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdocument">IFaxDocument</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
