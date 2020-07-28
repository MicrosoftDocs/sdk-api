---
UID: NS:strmif.AM_STREAM_INFO
title: AM_STREAM_INFO (strmif.h)
description: The AM_STREAM_INFO structure contains stream-control information.
helpviewer_keywords: ["AM_STREAM_INFO","AM_STREAM_INFO structure [DirectShow]","AM_STREAM_INFOStructure","dshow.am_stream_info","strmif/AM_STREAM_INFO"]
old-location: dshow\am_stream_info.htm
tech.root: dshow
ms.assetid: 63b62f03-1973-41af-b6a4-e1bcb6ab803f
ms.date: 12/05/2018
ms.keywords: AM_STREAM_INFO, AM_STREAM_INFO structure [DirectShow], AM_STREAM_INFOStructure, dshow.am_stream_info, strmif/AM_STREAM_INFO
f1_keywords:
- strmif/AM_STREAM_INFO
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- strmif.h
api_name:
- AM_STREAM_INFO
targetos: Windows
req.typenames: AM_STREAM_INFO
req.redist: 
ms.custom: 19H1
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

Bitwise combination of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-am_stream_info_flags">AM_STREAM_INFO_FLAGS</a> enumeration.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-getinfo">IAMStreamControl::GetInfo</a>
 

 

