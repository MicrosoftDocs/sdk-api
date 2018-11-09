---
UID: NE:codecapi.eAVEncH264VProfile
title: eAVEncH264VProfile
author: windows-sdk-content
description: Specifies an H.264 video profile.
old-location: mf\eavench264vprofile.htm
tech.root: medfound
ms.assetid: 143765ed-2d9e-4635-854a-0f3287e0e8e7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: codecapi/eAVEncH264VProfile, codecapi/eAVEncH264VProfile_422, codecapi/eAVEncH264VProfile_444, codecapi/eAVEncH264VProfile_Base, codecapi/eAVEncH264VProfile_ConstrainedBase, codecapi/eAVEncH264VProfile_Extended, codecapi/eAVEncH264VProfile_High, codecapi/eAVEncH264VProfile_High10, codecapi/eAVEncH264VProfile_Main, codecapi/eAVEncH264VProfile_MultiviewHigh, codecapi/eAVEncH264VProfile_ScalableBase, codecapi/eAVEncH264VProfile_ScalableHigh, codecapi/eAVEncH264VProfile_Simple, codecapi/eAVEncH264VProfile_StereoHigh, codecapi/eAVEncH264VProfile_UCConstrainedHigh, codecapi/eAVEncH264VProfile_UCScalableConstrainedBase, codecapi/eAVEncH264VProfile_UCScalableConstrainedHigh, codecapi/eAVEncH264VProfile_unknown, eAVEncH264VProfile, eAVEncH264VProfile enumeration [Media Foundation], eAVEncH264VProfile_422, eAVEncH264VProfile_444, eAVEncH264VProfile_Base, eAVEncH264VProfile_ConstrainedBase, eAVEncH264VProfile_Extended, eAVEncH264VProfile_High, eAVEncH264VProfile_High10, eAVEncH264VProfile_Main, eAVEncH264VProfile_MultiviewHigh, eAVEncH264VProfile_ScalableBase, eAVEncH264VProfile_ScalableHigh, eAVEncH264VProfile_Simple, eAVEncH264VProfile_StereoHigh, eAVEncH264VProfile_UCConstrainedHigh, eAVEncH264VProfile_UCScalableConstrainedBase, eAVEncH264VProfile_UCScalableConstrainedHigh, eAVEncH264VProfile_unknown, mf.eavench264vprofile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - eAVEncH264VProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncH264VProfile enumeration


## -description


Specifies an H.264 video profile.


## -enum-fields




### -field eAVEncH264VProfile_unknown

The profile is unknown or not specified.


### -field eAVEncH264VProfile_Simple

Simple profile.


### -field eAVEncH264VProfile_Base

Baseline profile.


### -field eAVEncH264VProfile_Main

Main profile.


### -field eAVEncH264VProfile_High

High profile.


### -field eAVEncH264VProfile_422

High 4:2:2 profile.


### -field eAVEncH264VProfile_High10

High 10 profile.


### -field eAVEncH264VProfile_444

High 4:4:4 profile.


### -field eAVEncH264VProfile_Extended

Extended profile.


### -field eAVEncH264VProfile_ScalableBase

Scalable base profile. H.264 extension.


### -field eAVEncH264VProfile_ScalableHigh

Scalable high profile. H.264 extension.


### -field eAVEncH264VProfile_MultiviewHigh

Multiview high profile. H.264 extension.


### -field eAVEncH264VProfile_StereoHigh

Stereo high profile. H.264 extension.


### -field eAVEncH264VProfile_ConstrainedBase

Constrained base profile. H.264 extension.


### -field eAVEncH264VProfile_UCConstrainedHigh

Constrained high profile. H.264 extension.


### -field eAVEncH264VProfile_UCScalableConstrainedBase

UC Constrained base profile. H.264 extension.


### -field eAVEncH264VProfile_UCScalableConstrainedHigh

UC Constrained high profile. H.264 extension.


## -remarks



These values are used with the <a href="https://msdn.microsoft.com/8c6a68cb-d976-4099-8934-064f0e8f6374">MF_MT_MPEG2_PROFILE</a> attribute.

These values are also used with <a href="https://msdn.microsoft.com/B3D500DF-1FD4-4D7C-B6F8-8DE4B957ED5C">H.264 UVC 1.5 camera encoders</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms705379(v=VS.85).aspx">Media Foundation Enumerations</a>
 

 

