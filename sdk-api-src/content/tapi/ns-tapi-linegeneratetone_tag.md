---
UID: NS:tapi.linegeneratetone_tag
title: linegeneratetone_tag
author: windows-sdk-content
description: The LINEGENERATETONE structure contains information about a tone to be generated. This structure is used by the lineGenerateTone and TSPI_lineGenerateTone functions.
old-location: tapi2\linegeneratetone_str.htm
old-project: tapi
ms.assetid: e430d944-816b-4072-a40b-b9001c465713
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPLINEGENERATETONE, LINEGENERATETONE, LINEGENERATETONE structure [TAPI 2.2], LPLINEGENERATETONE, LPLINEGENERATETONE structure pointer [TAPI 2.2], _tapi2_linegeneratetone_str, linegeneratetone_tag, tapi/LINEGENERATETONE, tapi/LPLINEGENERATETONE, tapi2.linegeneratetone_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
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
req.typenames: LINEGENERATETONE, *LPLINEGENERATETONE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEGENERATETONE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

