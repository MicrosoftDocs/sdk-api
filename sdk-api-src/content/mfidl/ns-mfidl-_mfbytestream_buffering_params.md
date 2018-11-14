---
UID: NS:mfidl._MFBYTESTREAM_BUFFERING_PARAMS
title: "_MFBYTESTREAM_BUFFERING_PARAMS"
author: windows-sdk-content
description: Specifies the buffering parameters for a network byte stream.
old-location: mf\mfbytestream_buffering_params.htm
tech.root: medfound
ms.assetid: 6667d32c-36a8-414e-a546-02d00a447b70
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 6667d32c-36a8-414e-a546-02d00a447b70, MFBYTESTREAM_BUFFERING_PARAMS, MFBYTESTREAM_BUFFERING_PARAMS structure [Media Foundation], _MFBYTESTREAM_BUFFERING_PARAMS, mf.mfbytestream_buffering_params, mfidl/MFBYTESTREAM_BUFFERING_PARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfidl.h
api_name:
 - MFBYTESTREAM_BUFFERING_PARAMS
product: Windows
targetos: Windows
req.typenames: MFBYTESTREAM_BUFFERING_PARAMS
req.redist: 
---

# _MFBYTESTREAM_BUFFERING_PARAMS structure


## -description



Specifies the buffering parameters for a network byte stream.




## -struct-fields




### -field cbTotalFileSize

Size of the file, in bytes. If the total size is unknown, set this member to -1.


### -field cbPlayableDataSize

Size of the playable media data in the file, excluding any trailing data that is not useful for playback. If this value is unknown, set this member to -1.


### -field prgBuckets

Pointer to an array of <a href="https://msdn.microsoft.com/aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e">MF_LEAKY_BUCKET_PAIR</a> structures. Each member of the array gives the buffer window for a particular bit rate.


### -field cBuckets

The number of elements in the <b>prgBuckets</b> array.


### -field qwNetBufferingTime

Amount of data to buffer from the network, in 100-nanosecond units. This value is in addition to the buffer windows defined in the <b>prgBuckets</b> member.


### -field qwExtraBufferingTimeDuringSeek

Amount of additional data to buffer when seeking, in 100-nanosecond units. This value reflects the fact that downloading must start from the previous key frame before the seek point. If the value is unknown, set this member to zero.


### -field qwPlayDuration

The playback duration of the file, in 100-nanosecond units. If the duration is unknown, set this member to zero.


### -field dRate

Playback rate.


## -see-also




<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

