---
UID: NE:codecapi.eAVEncCommonRateControlMode
title: eAVEncCommonRateControlMode
author: windows-sdk-content
description: Specifies the rate control mode for an encoder. This enumeration is used with the AVEncCommonRateControlMode codec property.
old-location: dshow\eavenccommonratecontrolmode.htm
old-project: DirectShow
ms.assetid: 6a8e538f-3d1e-4098-a001-a623c1212450
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: codecapi/eAVEncCommonRateControlMode, codecapi/eAVEncCommonRateControlMode_CBR, codecapi/eAVEncCommonRateControlMode_GlobalLowDelayVBR, codecapi/eAVEncCommonRateControlMode_GlobalVBR, codecapi/eAVEncCommonRateControlMode_LowDelayVBR, codecapi/eAVEncCommonRateControlMode_PeakConstrainedVBR, codecapi/eAVEncCommonRateControlMode_Quality, codecapi/eAVEncCommonRateControlMode_UnconstrainedVBR, dshow.eavenccommonratecontrolmode, eAVEncCommonRateControlMode, eAVEncCommonRateControlMode enumeration [DirectShow], eAVEncCommonRateControlModeEnumeration, eAVEncCommonRateControlMode_CBR, eAVEncCommonRateControlMode_GlobalLowDelayVBR, eAVEncCommonRateControlMode_GlobalVBR, eAVEncCommonRateControlMode_LowDelayVBR, eAVEncCommonRateControlMode_PeakConstrainedVBR, eAVEncCommonRateControlMode_Quality, eAVEncCommonRateControlMode_UnconstrainedVBR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncCommonRateControlMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVEncCommonRateControlMode enumeration


## -description



Specifies the rate control mode for an encoder. This enumeration is used with the <a href="https://msdn.microsoft.com/4a0d49b1-30da-4ebe-abff-3fceef6dd94a">AVEncCommonRateControlMode</a> codec property.




## -enum-fields




### -field eAVEncCommonRateControlMode_CBR

Constant bit rate (CBR) encoding.


### -field eAVEncCommonRateControlMode_PeakConstrainedVBR

Constrained variable bit rate (VBR) encoding.


### -field eAVEncCommonRateControlMode_UnconstrainedVBR

Unconstrained VBR encoding.


### -field eAVEncCommonRateControlMode_Quality

Quality-based VBR encoding. The encoder selects the bit rate to match a specified quality level. To specify the quality level, set the <a href="https://msdn.microsoft.com/2c7f3836-2392-47c6-9a56-d5a9b52560ff">AVEncCommonQuality</a> property.


### -field eAVEncCommonRateControlMode_LowDelayVBR

Low delay VBR encoding. H.264 extension.

Requires Windows 8.


### -field eAVEncCommonRateControlMode_GlobalVBR

Global VBR encoding. H.264 extension.

Requires Windows 8.


### -field eAVEncCommonRateControlMode_GlobalLowDelayVBR

Global low delay VBR encoding. H.264 extension.

Requires Windows 8.


## -remarks



This enumeration is also used with <a href="https://msdn.microsoft.com/B3D500DF-1FD4-4D7C-B6F8-8DE4B957ED5C">H.264 UVC 1.5 camera encoders</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

