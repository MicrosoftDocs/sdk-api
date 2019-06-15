---
UID: NS:tapi3if.TAPI_CUSTOMTONE
title: TAPI_CUSTOMTONE (tapi3if.h)
author: windows-sdk-content
description: The TAPI_CUSTOMTONE structure contains the parameters that define a custom tone.
old-location: tapi3\tapi_customtone_str.htm
tech.root: Tapi
ms.assetid: 1d3c7b25-92a8-41f5-8186-f6425cc6be74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPTAPI_CUSTOMTONE, TAPI_CUSTOMTONE, TAPI_CUSTOMTONE structure [TAPI 2.2], _tapi3_tapi_customtone_str, tapi3.tapi_customtone_str, tapi3if/TAPI_CUSTOMTONE"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: TAPI_CUSTOMTONE, *LPTAPI_CUSTOMTONE
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtones">ITLegacyCallMediaControl2::GenerateCustomTones</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatecustomtonesbycollection">ITLegacyCallMediaControl2::GenerateCustomTonesByCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linegeneratetone_tag">LINEGENERATETONE</a>
 

 

