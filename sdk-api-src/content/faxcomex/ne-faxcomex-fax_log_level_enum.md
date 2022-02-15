---
UID: NE:faxcomex.FAX_LOG_LEVEL_ENUM
title: FAX_LOG_LEVEL_ENUM (faxcomex.h)
description: The FAX_LOG_LEVEL_ENUM enumeration defines the event logging levels for a logging category.
helpviewer_keywords: ["FAX_LOG_LEVEL_ENUM","FAX_LOG_LEVEL_ENUM enumeration [Fax Service]","_mfax_fax_log_level_enum","fax._mfax_fax_log_level_enum","faxcomex/FAX_LOG_LEVEL_ENUM","faxcomex/fllMAX","faxcomex/fllMED","faxcomex/fllMIN","faxcomex/fllNONE","fllMAX","fllMED","fllMIN","fllNONE"]
old-location: fax\_mfax_fax_log_level_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7u3x.htm
ms.date: 12/05/2018
ms.keywords: FAX_LOG_LEVEL_ENUM, FAX_LOG_LEVEL_ENUM enumeration [Fax Service], _mfax_fax_log_level_enum, fax._mfax_fax_log_level_enum, faxcomex/FAX_LOG_LEVEL_ENUM, faxcomex/fllMAX, faxcomex/fllMED, faxcomex/fllMIN, faxcomex/fllNONE, fllMAX, fllMED, fllMIN, fllNONE
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
req.typenames: FAX_LOG_LEVEL_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_LOG_LEVEL_ENUM
 - faxcomex/FAX_LOG_LEVEL_ENUM
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
 - FAX_LOG_LEVEL_ENUM
---

# FAX_LOG_LEVEL_ENUM enumeration


## -description

The <b>FAX_LOG_LEVEL_ENUM</b> enumeration defines the event logging levels for a logging category.

## -enum-fields

### -field fllNONE:0

The fax server does not log events.

### -field fllMIN

The fax server logs only severe failure events, such as errors.

### -field fllMED

The fax server logs events of moderate severity, as well as severe failure events. This would include errors and warnings.

### -field fllMAX

The fax server logs all events.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging-generaleventslevel-vb">IFaxEventLogging::get_GeneralEventsLevel</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging-inboundeventslevel-vb">IFaxEventLogging::get_InboundEventsLevel</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging-initeventslevel-vb">IFaxEventLogging::get_InitEventsLevel</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxeventlogging-outboundeventslevel-vb">IFaxEventLogging::get_OutboundEventsLevel</a>
