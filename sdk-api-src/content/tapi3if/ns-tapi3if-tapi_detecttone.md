---
UID: NS:tapi3if.TAPI_DETECTTONE
title: TAPI_DETECTTONE
author: windows-sdk-content
description: The TAPI_DETECTTONE structure describes a tone to be monitored. This is used as an entry in an array.
old-location: tapi3\tapi_detecttone_str.htm
tech.root: TAPI
ms.assetid: c0e311e8-67b5-4dae-848e-589f306191fa
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "*LPTAPI_DETECTTONE, TAPI_DETECTTONE, TAPI_DETECTTONE structure [TAPI 2.2], _tapi3_tapi_detecttone_str, tapi3.tapi_detecttone_str, tapi3if/TAPI_DETECTTONE"
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
 - TAPI_DETECTTONE
product: Windows
targetos: Windows
req.typenames: TAPI_DETECTTONE, *LPTAPI_DETECTTONE
req.redist: 
---

# TAPI_DETECTTONE structure


## -description


The 
<b>TAPI_DETECTTONE</b> structure describes a tone to be monitored. This is used as an entry in an array.


## -struct-fields




### -field dwAppSpecific

Used by the application for tagging the tone. When this tone is detected, the value of the <b>dwAppSpecific</b> member is passed back to the application.


### -field dwDuration

The duration, in milliseconds, during which the tone should be present before a detection is made.


### -field dwFrequency1

The frequency, in hertz, of a component of the tone.


### -field dwFrequency2

The frequency, in hertz, of a component of the tone.


### -field dwFrequency3

The frequency, in hertz, of a component of the tone. If fewer than three frequencies are needed in the tone, a value of zero should be used for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be used for silence detection.


## -see-also




<a href="https://msdn.microsoft.com/e059bfc0-3701-4e07-8c30-0a2512731080">ITLegacyCallMediaControl2::DetectTones</a>



<a href="https://msdn.microsoft.com/09cbcd9d-66cd-4131-b45c-cb3898d8446d">ITLegacyCallMediaControl2::DetectTonesByCollection</a>



<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a>
 

 

