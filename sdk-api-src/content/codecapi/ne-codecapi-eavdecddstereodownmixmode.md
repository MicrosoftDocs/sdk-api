---
UID: NE:codecapi.eAVDecDDStereoDownMixMode
title: eAVDecDDStereoDownMixMode
author: windows-sdk-content
description: Specifies the stereo downmix mode for a Dolby Digital audio decoder.
old-location: mf\eavdecddstereodownmixmode.htm
tech.root: medfound
ms.assetid: B7DBC665-2942-433B-8C7F-1A02DB994A8B
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: codecapi/eAVDecDDStereoDownMixMode, codecapi/eAVDecDDStereoDownMixMode_Auto, codecapi/eAVDecDDStereoDownMixMode_LoRo, codecapi/eAVDecDDStereoDownMixMode_LtRt, eAVDecDDStereoDownMixMode, eAVDecDDStereoDownMixMode enumeration [Media Foundation], eAVDecDDStereoDownMixMode_Auto, eAVDecDDStereoDownMixMode_LoRo, eAVDecDDStereoDownMixMode_LtRt, mf.eavdecddstereodownmixmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVDecDDStereoDownMixMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVDecDDStereoDownMixMode enumeration


## -description


Specifies the stereo downmix mode for a Dolby Digital audio decoder. This enumeration is used with the <a href="https://msdn.microsoft.com/270893C6-8B44-4A4D-AE2B-2E58E260F649">CODECAPI_AVDecDDStereoDownMixMode</a> property.


## -enum-fields




### -field eAVDecDDStereoDownMixMode_Auto

The decoder selects the mode automatically.


### -field eAVDecDDStereoDownMixMode_LtRt

Left total/right total (Lt/Rt) downmix. (Surround compatible.)


### -field eAVDecDDStereoDownMixMode_LoRo

Left only/right only (Lo/Ro) downmix. (Stereo.)


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

