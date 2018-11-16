---
UID: NE:faxcomex.FAX_LOG_LEVEL_ENUM
title: FAX_LOG_LEVEL_ENUM
author: windows-sdk-content
description: The FAX_LOG_LEVEL_ENUM enumeration defines the event logging levels for a logging category.
old-location: fax\_mfax_fax_log_level_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7u3x.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FAX_LOG_LEVEL_ENUM, FAX_LOG_LEVEL_ENUM enumeration [Fax Service], _mfax_fax_log_level_enum, fax._mfax_fax_log_level_enum, faxcomex/FAX_LOG_LEVEL_ENUM, faxcomex/fllMAX, faxcomex/fllMED, faxcomex/fllMIN, faxcomex/fllNONE, fllMAX, fllMED, fllMIN, fllNONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_LOG_LEVEL_ENUM
product: Windows
targetos: Windows
req.typenames: FAX_LOG_LEVEL_ENUM
req.redist: 
---

# FAX_LOG_LEVEL_ENUM enumeration


## -description


The <b>FAX_LOG_LEVEL_ENUM</b> enumeration defines the event logging levels for a logging category.


## -enum-fields




### -field fllNONE

The fax server does not log events.


### -field fllMIN

The fax server logs only severe failure events, such as errors.


### -field fllMED

The fax server logs events of moderate severity, as well as severe failure events. This would include errors and warnings.


### -field fllMAX

The fax server logs all events.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685053(v=VS.85).aspx">IFaxEventLogging::get_GeneralEventsLevel</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685116(v=VS.85).aspx">IFaxEventLogging::get_InboundEventsLevel</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685042(v=VS.85).aspx">IFaxEventLogging::get_InitEventsLevel</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687455(v=VS.85).aspx">IFaxEventLogging::get_OutboundEventsLevel</a>
 

 

