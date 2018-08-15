---
UID: NS:eventtoken.EventRegistrationToken
title: EventRegistrationToken
author: windows-sdk-content
description: Identifies an event handler that has been registered with an event source.
old-location: winrt\eventregistrationtoken.htm
old-project: WinRT
ms.assetid: A98FE485-B3D8-4CD5-950F-765939F4672B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EventRegistrationToken, EventRegistrationToken structure [Windows Runtime], eventtoken/EventRegistrationToken, winrt.eventregistrationtoken
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: eventtoken.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EventRegistrationToken
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eventtoken.h
api_name:
 - EventRegistrationToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventRegistrationToken structure


## -description


Identifies an event handler that has been registered with an event source.


## -struct-fields




### -field value

Type: <b>INT64</b>

An identifying value that is provided by an event source. 


## -remarks



Use an <b>EventRegistrationToken</b> to  unsubscribe from a Windows Runtime event source.

You acquire an <b>EventRegistrationToken</b> when you subscribe to an event. 




## -see-also




<a href="https://msdn.microsoft.com/E9F74A4B-8678-4C40-8D6D-4779D7E5869E">IEventHandler<T></a>



<a href="https://msdn.microsoft.com/94B238FB-24F0-43FC-9F84-E30FE9081B50">ITypedEventHandler<TSender, TArgs></a>
 

 

