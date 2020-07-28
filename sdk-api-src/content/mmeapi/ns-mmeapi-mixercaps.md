---
UID: NS:mmeapi.tMIXERCAPS
title: MIXERCAPS (mmeapi.h)
description: The MIXERCAPS structure describes the capabilities of a mixer device.
helpviewer_keywords: ["*LPMIXERCAPS","*PMIXERCAPS","MIXERCAPS","MIXERCAPS structure [Windows Multimedia]","_win32_MIXERCAPS_str","mmeapi/MIXERCAPS","multimedia.mixercaps","tMIXERCAPS","tagMIXERCAPSA","tagMIXERCAPSW"]
old-location: multimedia\mixercaps.htm
tech.root: Multimedia
ms.assetid: 4a4220cb-fdb1-4afe-821f-27f5adb51530
ms.date: 12/05/2018
ms.keywords: '*LPMIXERCAPS, *PMIXERCAPS, MIXERCAPS, MIXERCAPS structure [Windows Multimedia], _win32_MIXERCAPS_str, mmeapi/MIXERCAPS, multimedia.mixercaps, tMIXERCAPS, tagMIXERCAPSA, tagMIXERCAPSW'
f1_keywords:
- mmeapi/MIXERCAPS
dev_langs:
- c++
req.header: mmeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- mmeapi.h
api_name:
- MIXERCAPS
targetos: Windows
req.typenames: MIXERCAPS, *PMIXERCAPS, *LPMIXERCAPS
req.redist: 
ms.custom: 19H1
---

# MIXERCAPS structure


## -description



The <b>MIXERCAPS</b> structure describes the capabilities of a mixer device.




## -struct-fields




### -field wMid

A manufacturer identifier for the mixer device driver. Manufacturer identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


### -field wPid

A product identifier for the mixer device driver. Product identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


### -field vDriverVersion

Version number of the mixer device driver. The high-order byte is the major version number, and the low-order byte is the minor version number.


### -field szPname

Name of the product. If the mixer device driver supports multiple cards, this string must uniquely and easily identify (potentially to a user) the specific card.


### -field fdwSupport

Various support information for the mixer device driver. No extended support bits are currently defined.


### -field cDestinations

The number of audio line destinations available through the mixer device. All mixer devices must support at least one destination line, so this member cannot be zero. Destination indexes used in the <b>dwDestination</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure range from zero to the value specified in the <b>cDestinations</b> member minus one.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



Audio Mixers



<a href="https://docs.microsoft.com/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a>
 

 

