---
UID: NS:strmif.AM_STREAM_INFO
title: AM_STREAM_INFO
author: windows-driver-content
description: The AM_STREAM_INFO structure contains stream-control information.
old-location: dshow\am_stream_info.htm
old-project: DirectShow
ms.assetid: 63b62f03-1973-41af-b6a4-e1bcb6ab803f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: AM_STREAM_INFO, AM_STREAM_INFO structure [DirectShow], AM_STREAM_INFOStructure, dshow.am_stream_info, strmif/AM_STREAM_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.typenames: AM_STREAM_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	AM_STREAM_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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
 

 

