---
UID: NS:eventtoken.EventRegistrationToken
title: EventRegistrationToken (eventtoken.h)
description: Identifies an event handler that has been registered with an event source.
helpviewer_keywords: ["EventRegistrationToken","EventRegistrationToken structure [Windows Runtime]","eventtoken/EventRegistrationToken","winrt.eventregistrationtoken"]
old-location: winrt\eventregistrationtoken.htm
tech.root: WinRT
ms.assetid: A98FE485-B3D8-4CD5-950F-765939F4672B
ms.date: 12/05/2018
ms.keywords: EventRegistrationToken, EventRegistrationToken structure [Windows Runtime], eventtoken/EventRegistrationToken, winrt.eventregistrationtoken
req.header: eventtoken.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventtoken.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EventRegistrationToken
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventRegistrationToken
 - eventtoken/EventRegistrationToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eventtoken.h
api_name:
 - EventRegistrationToken
---

# EventRegistrationToken structure (eventtoken.h)

## -description

Defines an event handler that has been registered with an event source.

## -struct-fields

### -field value

Type: **INT64**

An identifying value that is provided by an event source.

## -remarks

Use an **EventRegistrationToken** to  unsubscribe from a Windows Runtime event source.

You acquire an **EventRegistrationToken** when you subscribe to an event.

## -see-also

[IEventHandler\<T\> interface](/previous-versions/hh438424(v=vs.85))
