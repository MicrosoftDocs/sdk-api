---
UID: NE:strmif.AM_STREAM_INFO_FLAGS
title: AM_STREAM_INFO_FLAGS (strmif.h)
author: windows-sdk-content
description: The AM_STREAM_INFO_FLAGS enumeration defines flags that indicate a pin's stream-control status.
old-location: dshow\am_stream_info_flags.htm
tech.root: DirectShow
ms.assetid: 48f6ab36-f019-4096-b6e7-6f6ebc7c454a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AM_STREAM_INFO_DISCARDING, AM_STREAM_INFO_FLAGS, AM_STREAM_INFO_FLAGS , AM_STREAM_INFO_FLAGS enumeration [DirectShow], AM_STREAM_INFO_FLAGSEnumeration, AM_STREAM_INFO_START_DEFINED, AM_STREAM_INFO_STOP_DEFINED, AM_STREAM_INFO_STOP_SEND_EXTRA, dshow.am_stream_info_flags, strmif/AM_STREAM_INFO_DISCARDING, strmif/AM_STREAM_INFO_FLAGS, strmif/AM_STREAM_INFO_START_DEFINED, strmif/AM_STREAM_INFO_STOP_DEFINED, strmif/AM_STREAM_INFO_STOP_SEND_EXTRA
ms.topic: enum
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
 - AM_STREAM_INFO_FLAGS
product: Windows
targetos: Windows
req.typenames: AM_STREAM_INFO_FLAGS
req.redist: 
ms.custom: 19H1
---

# AM_STREAM_INFO_FLAGS enumeration


## -description



The <b>AM_STREAM_INFO_FLAGS</b> enumeration defines flags that indicate a pin's stream-control status.




## -enum-fields




### -field AM_STREAM_INFO_START_DEFINED

Indicates that the pin's start time is set.
          


### -field AM_STREAM_INFO_STOP_DEFINED

Indicates that the pin's stop time is been set.
          


### -field AM_STREAM_INFO_DISCARDING

Indicates that the pin is currently discarding data.
          


### -field AM_STREAM_INFO_STOP_SEND_EXTRA

Indicates that the pin will send one extra sample after it reaches the stop time.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_stream_info">AM_STREAM_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-getinfo">IAMStreamControl::GetInfo</a>
 

 

