---
UID: NS:mmreg.wavefilter_tag
title: wavefilter_tag
author: windows-sdk-content
description: The WAVEFILTER structure defines a filter for waveform-audio data.
old-location: multimedia\wavefilter.htm
tech.root: Multimedia
ms.assetid: dea3df47-88a2-439f-bf07-b5c592bf23e8
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*LPWAVEFILTER, *NPWAVEFILTER, *PWAVEFILTER, WAVEFILTER, WAVEFILTER structure [Windows Multimedia], _win32_WAVEFILTER_str, mmreg/WAVEFILTER, multimedia.wavefilter, wavefilter_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmreg.h
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
 - Mmreg.h
api_name:
 - WAVEFILTER
product: Windows
targetos: Windows
req.typenames: WAVEFILTER
req.redist: 
---

# wavefilter_tag structure


## -description



The <b>WAVEFILTER</b> structure defines a filter for waveform-audio data. Only filter information common to all waveform-audio data filters is included in this structure. For filters that require additional information, this structure is included as the first member in another structure along with the additional information.




## -struct-fields




### -field cbStruct

Size, in bytes, of the <b>WAVEFILTER</b> structure. The size specified in this member must be large enough to contain the base <b>WAVEFILTER</b> structure.


### -field dwFilterTag

Waveform-audio filter type. Filter tags are registered with Microsoft Corporation for various filter algorithms.


### -field fdwFilter

Flags for the <b>dwFilterTag</b> member. The flags defined for this member are universal to all filters. Currently, no flags are defined.


### -field dwReserved

Reserved for system use; should not be examined or modified by an application.


## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/4ae84ba8-f444-4d9e-adc8-343b4ee764cc">Waveform Structures</a>
 

 

