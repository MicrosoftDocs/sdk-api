---
UID: NE:evcoll._EC_SUBSCRIPTION_CONTENT_FORMAT
title: "_EC_SUBSCRIPTION_CONTENT_FORMAT"
author: windows-sdk-content
description: Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.
old-location: wec\ec_subscription_content_format.htm
old-project: WEC
ms.assetid: 72db596e-ef94-4167-bf1a-176095e17f8d
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EC_SUBSCRIPTION_CONTENT_FORMAT, EC_SUBSCRIPTION_CONTENT_FORMAT enumeration, EcContentFormatEvents, EcContentFormatRenderedText, _EC_SUBSCRIPTION_CONTENT_FORMAT, evcoll/EC_SUBSCRIPTION_CONTENT_FORMAT, evcoll/EcContentFormatEvents, evcoll/EcContentFormatRenderedText, wec.ec_subscription_content_format, wes.ec_subscription_content_format
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: EC_SUBSCRIPTION_CONTENT_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_CONTENT_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EC_SUBSCRIPTION_CONTENT_FORMAT enumeration


## -description


The <b>EC_SUBSCRIPTION_CONTENT_FORMAT</b> enumeration specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.


## -enum-fields




### -field EcContentFormatEvents

When an event is received, the Event Collector service sends an event as the received event to an event log. The service sends the raw event data only, and not any localized event data.


### -field EcContentFormatRenderedText

When an event is received, the Event Collector service sends an event as rendered text to an event log. The service sends raw event data and localized event information.

