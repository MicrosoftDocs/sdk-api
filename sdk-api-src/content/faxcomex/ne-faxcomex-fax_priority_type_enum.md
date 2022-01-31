---
UID: NE:faxcomex.FAX_PRIORITY_TYPE_ENUM
title: FAX_PRIORITY_TYPE_ENUM (faxcomex.h)
description: The FAX_PRIORITY_TYPE_ENUM enumeration defines the types of priorities for outbound faxes.
helpviewer_keywords: ["FAX_PRIORITY_TYPE_ENUM","FAX_PRIORITY_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_priority_type_enum","fax._mfax_fax_priority_type_enum","faxcomex/FAX_PRIORITY_TYPE_ENUM","faxcomex/fptHIGH","faxcomex/fptLOW","faxcomex/fptNORMAL","fptHIGH","fptLOW","fptNORMAL"]
old-location: fax\_mfax_fax_priority_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5oz1.htm
ms.date: 12/05/2018
ms.keywords: FAX_PRIORITY_TYPE_ENUM, FAX_PRIORITY_TYPE_ENUM enumeration [Fax Service], _mfax_fax_priority_type_enum, fax._mfax_fax_priority_type_enum, faxcomex/FAX_PRIORITY_TYPE_ENUM, faxcomex/fptHIGH, faxcomex/fptLOW, faxcomex/fptNORMAL, fptHIGH, fptLOW, fptNORMAL
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
req.typenames: FAX_PRIORITY_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_PRIORITY_TYPE_ENUM
 - faxcomex/FAX_PRIORITY_TYPE_ENUM
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
 - FAX_PRIORITY_TYPE_ENUM
---

# FAX_PRIORITY_TYPE_ENUM enumeration


## -description

The <b>FAX_PRIORITY_TYPE_ENUM</b> enumeration defines the types of priorities for outbound faxes.

## -enum-fields

### -field fptLOW:0

The fax will be sent with a low priority. All faxes that have a normal or a high priority will be sent before a fax that has a low priority.

### -field fptNORMAL

The fax will be sent with a normal priority. All faxes that have a high priority will be sent before a fax that has a normal priority.

### -field fptHIGH

The fax will be sent with a high priority.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument-priority-vb">IFaxDocument::get_Priority</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-priority-vb">IFaxOutgoingJob::get_Priority</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-priority-vb">IFaxOutgoingMessage::get_Priority</a>
