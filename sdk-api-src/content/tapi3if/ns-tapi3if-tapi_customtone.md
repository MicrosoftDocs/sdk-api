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

# TAPI_CUSTOMTONE structure


## -description


The 
<b>TAPI_CUSTOMTONE</b> structure contains the parameters that define a custom tone.


## -struct-fields




### -field dwFrequency

The frequency, in hertz, of the tone.


### -field dwCadenceOn

The "on" duration, in milliseconds, of the cadence of a custom tone.


### -field dwCadenceOff

The "off" duration, in milliseconds, of the cadence of a custom tone.


### -field dwVolume

The volume level at which to generate the tone.


## -see-also




<a href="https://msdn.microsoft.com/fcc5d3c9-a7ab-4467-a948-b9fd68afe7b4">ITLegacyCallMediaControl2::GenerateCustomTones</a>



<a href="https://msdn.microsoft.com/5115192e-68de-4779-92dc-7cf63585faae">ITLegacyCallMediaControl2::GenerateCustomTonesByCollection</a>



<a href="https://msdn.microsoft.com/e430d944-816b-4072-a40b-b9001c465713">LINEGENERATETONE</a>
 

 

