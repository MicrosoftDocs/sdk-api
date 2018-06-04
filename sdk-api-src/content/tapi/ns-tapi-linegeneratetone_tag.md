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

# linegeneratetone_tag structure


## -description


The 
<b>LINEGENERATETONE</b> structure contains information about a tone to be generated. This structure is used by the 
<a href="https://msdn.microsoft.com/d5975bd0-2406-45a8-9631-80f40a860204">lineGenerateTone</a> and 
<a href="https://msdn.microsoft.com/195d0974-ff0f-4274-9278-5276512fcba4">TSPI_lineGenerateTone</a> functions.


## -struct-fields




### -field dwFrequency

Frequency of this tone component, in hertz. A service provider may adjust (round up or down) the frequency specified by the application to fit its resolution.


### -field dwCadenceOn

Length of the "on" duration of the cadence of the custom tone to be generated, in milliseconds. Zero means no tone is generated.


### -field dwCadenceOff

Length of the "off" duration of the cadence of the custom tone to be generated, in milliseconds. Zero means no off time, that is, a constant tone.


### -field dwVolume

Volume level at which the tone is to be generated. A value of 0x0000FFFF represents full volume, and a value of 0x00000000 is silence.


## -remarks



This structure may not be extended.

This structure is used only for the generation of tones. It is not used for tone monitoring.




## -see-also




<a href="https://msdn.microsoft.com/195d0974-ff0f-4274-9278-5276512fcba4">TSPI_lineGenerateTone</a>



<a href="https://msdn.microsoft.com/d5975bd0-2406-45a8-9631-80f40a860204">lineGenerateTone</a>
 

 

