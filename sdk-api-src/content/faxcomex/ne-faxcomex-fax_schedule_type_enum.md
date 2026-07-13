---
UID: NE:faxcomex.FAX_SCHEDULE_TYPE_ENUM
title: FAX_SCHEDULE_TYPE_ENUM (faxcomex.h)
description: The FAX_SCHEDULE_TYPE_ENUM enumeration defines the types of scheduling for outbound faxes.
helpviewer_keywords: ["FAX_SCHEDULE_TYPE_ENUM","FAX_SCHEDULE_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_schedule_type_enum","fax._mfax_fax_schedule_type_enum","faxcomex/FAX_SCHEDULE_TYPE_ENUM","faxcomex/fstDISCOUNT_PERIOD","faxcomex/fstNOW","faxcomex/fstSPECIFIC_TIME","fstDISCOUNT_PERIOD","fstNOW","fstSPECIFIC_TIME"]
old-location: fax\_mfax_fax_schedule_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5ust.htm
ms.date: 12/05/2018
ms.keywords: FAX_SCHEDULE_TYPE_ENUM, FAX_SCHEDULE_TYPE_ENUM enumeration [Fax Service], _mfax_fax_schedule_type_enum, fax._mfax_fax_schedule_type_enum, faxcomex/FAX_SCHEDULE_TYPE_ENUM, faxcomex/fstDISCOUNT_PERIOD, faxcomex/fstNOW, faxcomex/fstSPECIFIC_TIME, fstDISCOUNT_PERIOD, fstNOW, fstSPECIFIC_TIME
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_SCHEDULE_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_SCHEDULE_TYPE_ENUM
 - faxcomex/FAX_SCHEDULE_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_SCHEDULE_TYPE_ENUM
---

# FAX_SCHEDULE_TYPE_ENUM enumeration


## -description

The <b>FAX_SCHEDULE_TYPE_ENUM</b> enumeration defines the types of scheduling for outbound faxes.

## -enum-fields

### -field fstNOW:0

Send the fax as soon as a device is available.

### -field fstSPECIFIC_TIME

Send the fax no sooner than the specified time. The actual time that the fax will be sent depends on device availability and fax priority.

### -field fstDISCOUNT_PERIOD

Send the fax during the discount rate period.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-scheduletime-vb">IFaxDocument::get_ScheduleTime</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-scheduletype-vb">IFaxDocument::get_ScheduleType</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-discountrateend-vb">IFaxOutgoingQueue::get_DiscountRateEnd</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-discountratestart-vb">IFaxOutgoingQueue::get_DiscountRateStart</a>
