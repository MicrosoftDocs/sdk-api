---
UID: NS:xaudio2fx.XAUDIO2FX_VOLUMEMETER_LEVELS
title: XAUDIO2FX_VOLUMEMETER_LEVELS
author: windows-sdk-content
description: Describes parameters for use with the volume meter APO.
old-location: xaudio2\xaudio2fx_volumemeter_levels.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2FX_VOLUMEMETER_LEVELS
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: XAUDIO2FX_VOLUMEMETER_LEVELS, XAUDIO2FX_VOLUMEMETER_LEVELS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2fx_volumemeter_levels, xaudio2fx/XAUDIO2FX_VOLUMEMETER_LEVELS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xaudio2fx.h
req.include-header: 
req.redist: 
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
req.typenames: XAUDIO2FX_VOLUMEMETER_LEVELS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2fx.h
api_name:
 - XAUDIO2FX_VOLUMEMETER_LEVELS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAUDIO2FX_VOLUMEMETER_LEVELS structure


## -description


Describes parameters for use with the volume meter APO.


## -struct-fields




### -field pPeakLevels

Array that will be filled with the maximum absolute level for each channel during a processing pass. The array must be at least <i>ChannelCount</i> × sizeof(float) bytes. <i>pPeakLevels</i> may be NULL if <i>pRMSLevels</i> is not NULL.


### -field pRMSLevels

Array that will be filled with root mean square level for each channel during a processing pass. The array must be at least <i>ChannelCount</i> × sizeof(float) bytes. <i>pRMSLevels</i> may be NULL if <i>pPeakLevels</i> is not NULL.


### -field ChannelCount

Number of channels being processed.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/75CC5E5D-74B2-4972-9E1D-D6CB4A3034CD">XAudio2 IXAudio2Voice::GetEffectParameters</a> method.



<i>pPeakLevels</i> and <i>pRMSLevels</i> are not returned by <a href="https://msdn.microsoft.com/75CC5E5D-74B2-4972-9E1D-D6CB4A3034CD">IXAudio2Voice::GetEffectParameters</a>, the arrays are only filled out if they are present. If <i>pPeakLevels</i> and <i>pRMSLevels</i> are used they must be allocated by the application. The application is responsible for freeing the arrays when they are no longer needed.



<i>ChannelCount</i> must be set by the application to match the number of channels in the voice the effect is applied to.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4c33bd83-2654-cd6f-ea6c-bbc0d5872638">How to: Create an Effect Chain</a>



<a href="https://msdn.microsoft.com/7A5217AE-D7D6-4D92-A14E-DA36854F4D3E">IXAudio2Voice::SetEffectParameters</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio Structures</a>



<a href="https://msdn.microsoft.com/c997dfe5-2207-422c-968c-9a6acd818d50">XAudio2CreateVolumeMeter</a>
 

 

