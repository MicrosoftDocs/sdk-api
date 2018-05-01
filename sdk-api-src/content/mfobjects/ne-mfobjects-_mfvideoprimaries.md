---
UID: NE:mfobjects._MFVideoPrimaries
title: "_MFVideoPrimaries"
author: windows-driver-content
description: Specifies the color primaries of a video source.
old-location: mf\mfvideoprimaries.htm
old-project: medfound
ms.assetid: a1d6a60c-823c-46c3-a751-18e55fbc52a1
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: MFVideoPrimaries, MFVideoPrimaries enumeration [Media Foundation], MFVideoPrimaries_ACES, MFVideoPrimaries_BT2020, MFVideoPrimaries_BT470_2_SysBG, MFVideoPrimaries_BT470_2_SysM, MFVideoPrimaries_BT709, MFVideoPrimaries_DCI_P3, MFVideoPrimaries_EBU3213, MFVideoPrimaries_ForceDWORD, MFVideoPrimaries_Last, MFVideoPrimaries_SMPTE170M, MFVideoPrimaries_SMPTE240M, MFVideoPrimaries_SMPTE_C, MFVideoPrimaries_Unknown, MFVideoPrimaries_XYZ, MFVideoPrimaries_reserved, _MFVideoPrimaries, a1d6a60c-823c-46c3-a751-18e55fbc52a1, mf.mfvideoprimaries, mfobjects/MFVideoPrimaries, mfobjects/MFVideoPrimaries_ACES, mfobjects/MFVideoPrimaries_BT2020, mfobjects/MFVideoPrimaries_BT470_2_SysBG, mfobjects/MFVideoPrimaries_BT470_2_SysM, mfobjects/MFVideoPrimaries_BT709, mfobjects/MFVideoPrimaries_DCI_P3, mfobjects/MFVideoPrimaries_EBU3213, mfobjects/MFVideoPrimaries_ForceDWORD, mfobjects/MFVideoPrimaries_Last, mfobjects/MFVideoPrimaries_SMPTE170M, mfobjects/MFVideoPrimaries_SMPTE240M, mfobjects/MFVideoPrimaries_SMPTE_C, mfobjects/MFVideoPrimaries_Unknown, mfobjects/MFVideoPrimaries_XYZ, mfobjects/MFVideoPrimaries_reserved
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFVideoPrimaries
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfobjects.h
api_name:
-	MFVideoPrimaries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

