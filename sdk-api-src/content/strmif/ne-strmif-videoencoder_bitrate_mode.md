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

# VIDEOENCODER_BITRATE_MODE enumeration


## -description



The <b>VIDEOENCODER_BITRATE_MODE</b> enumeration type defines the three types of bitrates supported by the <a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> interface.




## -enum-fields




### -field ConstantBitRate

The bit rate used for encoding is constant.
          


### -field VariableBitRateAverage

The bit rate used for encoding is variable with the specified bitrate used as a guaranteed average over a specified window. The default window size is considered to be five minutes.
          


### -field VariableBitRatePeak


            The <b>ENCAPIPARAM_BITRATE</b> value is the expected (not guaranteed) average bit rate over a given time period and that the <b>ENCAPIPARAM_PEAK_BITRATE</b> value is the peak which the bit rate must not exceed. The default window size is considered to be 500ms (which is traditionally equal to one GOP).
          


## -see-also




<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a>
 

 

