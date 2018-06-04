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

# _MFWaveFormatExConvertFlags enumeration


## -description



Contains flags that specify how to convert an audio media type.




## -enum-fields




### -field MFWaveFormatExConvertFlag_Normal

Convert the media type to a <b>WAVEFORMATEX</b> structure if possible, or a <b>WAVEFORMATEXTENSIBLE</b> structure otherwise.


### -field MFWaveFormatExConvertFlag_ForceExtensible

Convert the media type to a <b>WAVEFORMATEXTENSIBLE</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/b124bac2-90de-4358-a079-f509a89c3776">MFCreateWaveFormatExFromMFMediaType</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

