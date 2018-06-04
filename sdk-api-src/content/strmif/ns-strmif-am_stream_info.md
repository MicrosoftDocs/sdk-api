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

# AM_STREAM_INFO structure


## -description



The AM_STREAM_INFO structure contains stream-control information.




## -struct-fields




### -field tStart

Time when the pin will start streaming data.


### -field tStop

Time when the pin will stop streaming data.


### -field dwStartCookie

Value that will be sent with the event notification when the pin starts.


### -field dwStopCookie

Value that will be sent with the event notification when the pin stops.


### -field dwFlags

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/48f6ab36-f019-4096-b6e7-6f6ebc7c454a">AM_STREAM_INFO_FLAGS</a> enumeration.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/9993534c-ec93-4c15-b977-6a0933d23a72">IAMStreamControl::GetInfo</a>
 

 

