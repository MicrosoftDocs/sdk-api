---
UID: NE:faxcomex.FAX_LOG_LEVEL_ENUM
title: FAX_LOG_LEVEL_ENUM
author: windows-sdk-content
description: The FAX_LOG_LEVEL_ENUM enumeration defines the event logging levels for a logging category.
old-location: fax\_mfax_fax_log_level_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7u3x.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FAX_LOG_LEVEL_ENUM, FAX_LOG_LEVEL_ENUM enumeration [Fax Service], _mfax_fax_log_level_enum, fax._mfax_fax_log_level_enum, faxcomex/FAX_LOG_LEVEL_ENUM, faxcomex/fllMAX, faxcomex/fllMED, faxcomex/fllMIN, faxcomex/fllNONE, fllMAX, fllMED, fllMIN, fllNONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FAX_LOG_LEVEL_ENUM
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
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
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




<a href="https://msdn.microsoft.com/8ab80241-44ab-49e3-97b9-d4c0e8cfa096">IFaxEventLogging::get_GeneralEventsLevel</a>



<a href="https://msdn.microsoft.com/aa223f94-cc2b-4704-9b57-22e1cb7d1a89">IFaxEventLogging::get_InboundEventsLevel</a>



<a href="https://msdn.microsoft.com/5a8f73d1-c612-4589-91bc-84a4659faefd">IFaxEventLogging::get_InitEventsLevel</a>



<a href="https://msdn.microsoft.com/115e661c-4f44-4ed3-a591-ffa89d55d72b">IFaxEventLogging::get_OutboundEventsLevel</a>
 

 

