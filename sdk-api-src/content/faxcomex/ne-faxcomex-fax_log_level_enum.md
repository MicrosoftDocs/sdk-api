---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

