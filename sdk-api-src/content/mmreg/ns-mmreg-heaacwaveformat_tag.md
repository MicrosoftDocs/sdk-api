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

# heaacwaveformat_tag structure


## -description


Contains format data for an AAC or HE-AAC stream that includes AudioSpecificConfig() data.


## -struct-fields




### -field wfInfo

A <a href="https://msdn.microsoft.com/a9b888fb-b4a5-44c3-a715-687cc751063d">HEAACWAVEINFO</a> structure. 


### -field pbAudioSpecificConfig

A byte array that contains the value of AudioSpecificConfig(), as defined by ISO/IEC 14496-3. The array might be larger than the size given in the structure declaration. Use the value of <b>wfInfo.wfx.cbSize</b>  to determine the size.




## -remarks



Use this structure to access the AudioSpecificConfig() data that follows an <a href="https://msdn.microsoft.com/a9b888fb-b4a5-44c3-a715-687cc751063d">HEAACWAVEINFO</a> structure. This data is present only when the <b>wStructType</b> member of the <b>HEAACWAVEFORMAT</b> structure is zero.



