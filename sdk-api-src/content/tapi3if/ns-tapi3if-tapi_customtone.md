---
UID: NS:tapi3if.TAPI_CUSTOMTONE
title: TAPI_CUSTOMTONE
author: windows-sdk-content
description: The TAPI_CUSTOMTONE structure contains the parameters that define a custom tone.
old-location: tapi3\tapi_customtone_str.htm
old-project: Tapi
ms.assetid: 1d3c7b25-92a8-41f5-8186-f6425cc6be74
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPTAPI_CUSTOMTONE, TAPI_CUSTOMTONE, TAPI_CUSTOMTONE structure [TAPI 2.2], _tapi3_tapi_customtone_str, tapi3.tapi_customtone_str, tapi3if/TAPI_CUSTOMTONE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi3if.h
req.include-header: 
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
tech.root: 
req.typenames: TAPI_CUSTOMTONE, *LPTAPI_CUSTOMTONE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TAPI_CUSTOMTONE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

