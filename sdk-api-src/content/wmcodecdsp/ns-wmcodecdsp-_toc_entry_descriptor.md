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

# _TOC_ENTRY_DESCRIPTOR structure


## -description


The <b>TOC_ENTRY_DESCRIPTOR</b> structure holds descriptive information for an entry in a table of contents. An entry in a table of contents describes a portion of a media file. For example, an entry might describe a ten-second chunk of video that  starts 90 seconds after the beginning of a video file.


## -struct-fields




### -field qwStartTime

The start time, in 100-nanosecond units, of the portion of a media file represented by an entry in a table of contents.


### -field qwEndTime

The end time, in 100-nanosecond units, of the portion of a media file represented by an entry in a table of contents.


### -field qwStartPacketOffset

Not used.


### -field qwEndPacketOffset

Not used.


### -field qwRepresentativeFrameTime

The presentation time, in 100-nanosecond units, of a frame that is a good representation of the entry. This frame could be used for a thumbnail image that represents the entry.


## -see-also




<a href="https://msdn.microsoft.com/7438b09e-e649-462d-9a36-fb19e0817d75">Table of Contents Parser Structures</a>
 

 

