---
UID: NS:strmif.tagQuality
title: tagQuality
author: windows-sdk-content
description: The Quality structure describes a quality message by indicating Flood or Famine in the renderer and specifying the percentage of frames to drop or add to optimize the renderer's performance.
old-location: dshow\quality.htm
tech.root: DirectShow
ms.assetid: 2ab7fcde-0e44-4d60-acf5-3638efbe15f7
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: Quality, Quality structure [DirectShow], QualityStructure, dshow.quality, strmif/Quality, tagQuality
ms.prod: windows
ms.technology: windows-sdk
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
 - Quality
product: Windows
targetos: Windows
req.typenames: Quality
req.redist: 
---

# tagQuality structure


## -description



The <code>Quality</code> structure describes a quality message by indicating Flood or Famine in the renderer and specifying the percentage of frames to drop or add to optimize the renderer's performance.




## -struct-fields




### -field Type

Value from the <a href="https://msdn.microsoft.com/54a2239d-bf37-499d-b8c4-f797c1b46933">QualityMessageType</a> enumeration, indicating whether the downstream filter needs more or less data.


### -field Proportion

Value that specifies the rate at which DirectShow should continue to send media samples. The base value is 1000, which indicates there should be no change. A percentage increase or decrease from 1000 indicates the percentage of frames to add or drop. If this value is 800, for example, DirectShow will drop 20 percent of the incoming frames to match the renderer's speed.


### -field Late

If a famine exists downstream, this is the amount of time by which the stream is lagging.


### -field TimeStamp

Value that specifies the time when DirectShow created this structure, which is usually the start time on a video sample.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

