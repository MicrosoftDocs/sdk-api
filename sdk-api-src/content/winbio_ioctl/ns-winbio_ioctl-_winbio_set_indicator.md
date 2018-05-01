---
UID: NS:winbio_ioctl._WINBIO_SET_INDICATOR
title: "_WINBIO_SET_INDICATOR"
author: windows-driver-content
description: The WINBIO_SET_INDICATOR structure is the IN payload for IOCTL_BIOMETRIC_SET_INDICATOR.
old-location: biometric\winbio_set_indicator.htm
old-project: biometric
ms.assetid: c4410845-3c7b-445e-80ec-25694b122a0e
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: "*PWINBIO_SET_INDICATOR, PWINBIO_SET_INDICATOR, PWINBIO_SET_INDICATOR structure pointer [Biometric Devices], WINBIO_SET_INDICATOR, WINBIO_SET_INDICATOR structure [Biometric Devices], _WINBIO_SET_INDICATOR, biometric.winbio_set_indicator, biometric_ref_2ee60af8-1872-4932-9db7-9c3c27e29ddf.xml, winbio_ioctl/PWINBIO_SET_INDICATOR, winbio_ioctl/WINBIO_SET_INDICATOR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_ioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
req.typenames: WINBIO_SET_INDICATOR, *PWINBIO_SET_INDICATOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_ioctl.h
api_name:
-	WINBIO_SET_INDICATOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_SET_INDICATOR structure


## -description


The WINBIO_SET_INDICATOR structure is the IN payload for <a href="https://msdn.microsoft.com/library/windows/hardware/ff536441">IOCTL_BIOMETRIC_SET_INDICATOR</a>.


## -struct-fields




### -field PayloadSize

Specifies the total size of the payload, which includes the fixed length structure and any variable data at the end.


### -field IndicatorStatus

Specifies a WINBIO_INDICATOR_STATUS that indicates whether the indicator light should be set on or off.

 Possible values are shown in the following table. 

<table>
<tr>
<td>
Indicator status code

</td>
<td>
Description

</td>
</tr>
<tr>
<td>
WINBIO_INDICATOR_ON

</td>
<td>
The indicator light is on, and changes according to the sensor status.  To be able to set WINBIO_INDICATOR_ON, you must set WINBIO_CAPABILITY_INDICATOR in the <b>Capabilities</b> member of the WINBIO_SENSOR_ATTRIBUTES structure.

</td>
</tr>
<tr>
<td>
WINBIO_INDICATOR_OFF

</td>
<td>
The sensor indicator light is off.  Sensors that do not have an indicator light will always return this value in IOCTL_GET_SENSOR_STATUS. 

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536441">IOCTL_BIOMETRIC_SET_INDICATOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536471">WINBIO_GET_INDICATOR</a>
 

 

