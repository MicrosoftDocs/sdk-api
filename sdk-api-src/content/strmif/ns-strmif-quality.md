---
UID: NS:strmif.tagQuality
title: Quality (strmif.h)
description: The Quality structure describes a quality message by indicating Flood or Famine in the renderer and specifying the percentage of frames to drop or add to optimize the renderer's performance.
old-location: dshow\quality.htm
tech.root: DirectShow
ms.assetid: 2ab7fcde-0e44-4d60-acf5-3638efbe15f7
ms.date: 12/05/2018
ms.keywords: Quality, Quality structure [DirectShow], QualityStructure, dshow.quality, strmif/Quality
ms.topic: struct
f1_keywords:
- strmif/Quality
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
- Quality
targetos: Windows
req.typenames: Quality
req.redist: 
ms.custom: 19H1
---

# Quality structure


## -description



The <code>Quality</code> structure describes a quality message by indicating Flood or Famine in the renderer and specifying the percentage of frames to drop or add to optimize the renderer's performance.




## -struct-fields




### -field Type

Value from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-qualitymessagetype">QualityMessageType</a> enumeration, indicating whether the downstream filter needs more or less data.


### -field Proportion

Value that specifies the rate at which DirectShow should continue to send media samples. The base value is 1000, which indicates there should be no change. A percentage increase or decrease from 1000 indicates the percentage of frames to add or drop. If this value is 800, for example, DirectShow will drop 20 percent of the incoming frames to match the renderer's speed.


### -field Late

If a famine exists downstream, this is the amount of time by which the stream is lagging.


### -field TimeStamp

Value that specifies the time when DirectShow created this structure, which is usually the start time on a video sample.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

