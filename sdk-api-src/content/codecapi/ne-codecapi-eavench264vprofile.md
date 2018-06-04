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




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

