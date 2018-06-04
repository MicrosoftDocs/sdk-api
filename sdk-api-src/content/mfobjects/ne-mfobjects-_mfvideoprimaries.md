---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MFVideoPrimaries enumeration


## -description


Specifies the color primaries of a video source. The color primaries define how to convert colors from RGB color space to CIE XYZ color space.


## -enum-fields




### -field MFVideoPrimaries_Unknown


            The color primaries are unknown.
          


### -field MFVideoPrimaries_reserved


            Reserved.
          


### -field MFVideoPrimaries_BT709


            ITU-R BT.709. Also used for sRGB and scRGB.
          


### -field MFVideoPrimaries_BT470_2_SysM


            ITU-R BT.470-4 System M (NTSC).
          


### -field MFVideoPrimaries_BT470_2_SysBG


            ITU-R BT.470-4 System B,G (NTSC).
          


### -field MFVideoPrimaries_SMPTE170M


            SMPTE 170M.
          


### -field MFVideoPrimaries_SMPTE240M


            SMPTE 240M.
          


### -field MFVideoPrimaries_EBU3213


            EBU 3213.
          


### -field MFVideoPrimaries_SMPTE_C


            SMPTE C (SMPTE RP 145).
          


### -field MFVideoPrimaries_BT2020

ITU-R BT.2020 color primaries.

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>

### -field MFVideoPrimaries_XYZ

CIE 1931 XYZ (see: <a href="https://en.wikipedia.org/wiki/CIE_1931_color_space">CIE 1931 color space</a>).  Note that this color space is only well-defined for floating point representations.

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>

### -field MFVideoPrimaries_DCI_P3

DCI-P3

<div class="alert"><b>Note</b>  Requires Windows 10, version 1703 or later.</div>
<div> </div>

### -field MFVideoPrimaries_ACES

Academy Color Encoding System

<div class="alert"><b>Note</b>  Requires Windows 10, version 1703 or later.</div>
<div> </div>

### -field MFVideoPrimaries_Last


            Reserved.
          


### -field MFVideoPrimaries_ForceDWORD


            Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.
          


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/56f31c1a-b610-4da0-9df4-76e15add672c">MF_MT_VIDEO_PRIMARIES</a> attribute.

For more information about these values, see the remarks for the <a href="https://msdn.microsoft.com/4534a198-cf6c-4689-9fe4-0e5cdc7ce26a">DXVA2_VideoPrimaries</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

