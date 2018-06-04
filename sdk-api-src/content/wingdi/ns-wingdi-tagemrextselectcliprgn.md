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

# tagEMREXTSELECTCLIPRGN structure


## -description



The <b>EMREXTSELECTCLIPRGN</b> structure contains members for the <a href="https://msdn.microsoft.com/d222defe-2ef9-4622-b2e1-462a91cb1b0a">ExtSelectClipRgn</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field cbRgnData

Size of region data, in bytes.


### -field iMode

Operation to be performed. This member must be one of the following values: RGN_AND, RGN_COPY, RGN_DIFF, RGN_OR, or RGN_XOR.


### -field RgnData

Buffer containing a <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/d222defe-2ef9-4622-b2e1-462a91cb1b0a">ExtSelectClipRgn</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

