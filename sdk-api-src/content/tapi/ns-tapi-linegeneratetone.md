---
UID: NS:tapi.linegeneratetone_tag
title: LINEGENERATETONE (tapi.h)
author: windows-sdk-content
description: The LINEGENERATETONE structure contains information about a tone to be generated. This structure is used by the lineGenerateTone and TSPI_lineGenerateTone functions.
old-location: tapi2\linegeneratetone_str.htm
tech.root: Tapi
ms.assetid: e430d944-816b-4072-a40b-b9001c465713
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINEGENERATETONE, LINEGENERATETONE, LINEGENERATETONE structure [TAPI 2.2], LPLINEGENERATETONE, LPLINEGENERATETONE structure pointer [TAPI 2.2], _tapi2_linegeneratetone_str, tapi/LINEGENERATETONE, tapi/LPLINEGENERATETONE, tapi2.linegeneratetone_str"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: LINEGENERATETONE, *LPLINEGENERATETONE
req.redist: 
ms.custom: 19H1
---

# LINEGENERATETONE structure


## -description


The 
<b>LINEGENERATETONE</b> structure contains information about a tone to be generated. This structure is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegeneratetone">lineGenerateTone</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegeneratetone">TSPI_lineGenerateTone</a> functions.


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




<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegeneratetone">TSPI_lineGenerateTone</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegeneratetone">lineGenerateTone</a>
 

 

