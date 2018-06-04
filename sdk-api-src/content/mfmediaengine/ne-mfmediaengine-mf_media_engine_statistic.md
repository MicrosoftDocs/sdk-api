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

# MF_MEDIA_ENGINE_STATISTIC enumeration


## -description


Identifies statistics that the Media Engine tracks during playback. To get a playback statistic from the Media Engine, call <a href="https://msdn.microsoft.com/3C2FDE86-2EBD-4A5C-BD02-90613DBFDE65">IMFMediaEngineEx::GetStatistics</a>.

In the descriptions that follow, the data type and value-type tag for the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> are listed in parentheses.


## -enum-fields




### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_RENDERED

The number of rendered video frames. (<b>ULONG</b>, <b>VT_UI4</b>)


### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_DROPPED

The number of dropped video frames. (<b>ULONG</b>, <b>VT_UI4</b>)


### -field MF_MEDIA_ENGINE_STATISTIC_BYTES_DOWNLOADED

The number of bytes that have been downloaded since the last HTTP range request. (<b>ULARGE_INTEGER</b>, <b>VT_UI8</b>).


### -field MF_MEDIA_ENGINE_STATISTIC_BUFFER_PROGRESS

The percentage of the playout buffer filled during buffering. The value is an integer in the range 0–100. (<b>LONG</b>, <b>VT_I4</b>)


### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_PER_SECOND

The frames per second. (<b>FLOAT</b>, <b>VT_R4</b>)


### -field MF_MEDIA_ENGINE_STATISTIC_PLAYBACK_JITTER

The amount of playback jitter. (<b>DOUBLE</b>, <b>VT_R8</b>)

Supported in Windows 8.1 and later.


### -field MF_MEDIA_ENGINE_STATISTIC_FRAMES_CORRUPTED

The number of corrupted frames. (<b>ULONG</b>, <b>VT_UI4</b>)

Supported in Windows 8.1 and later.


### -field MF_MEDIA_ENGINE_STATISTIC_TOTAL_FRAME_DELAY

The total amount of frame delay.  (<b>DOUBLE</b>, <b>VT_R8</b>)

Supported in Windows 8.1 and later.


## -see-also




<a href="https://msdn.microsoft.com/3C2FDE86-2EBD-4A5C-BD02-90613DBFDE65">IMFMediaEngineEx::GetStatistics</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

