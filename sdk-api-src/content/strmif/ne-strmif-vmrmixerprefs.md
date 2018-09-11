---
UID: NE:strmif.VMRMixerPrefs
title: VMRMixerPrefs
author: windows-sdk-content
description: The VMRMixerPrefs enumeration contains flags that specify decimation, filtering, and color space information that will be used when the video image is created on the DirectDraw surface.
old-location: dshow\vmrmixerprefs.htm
tech.root: DirectShow
ms.assetid: 0852590c-6bca-4261-99c0-fff8a012f18e
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: MixerPref_ARAdjustXorY, MixerPref_BiLinearFiltering, MixerPref_DecimateMask, MixerPref_DecimateOutput, MixerPref_DecimationReserved, MixerPref_DynamicDecimateBy2, MixerPref_DynamicMask, MixerPref_DynamicReserved, MixerPref_DynamicSwitchToBOB, MixerPref_FilteringMask, MixerPref_NoDecimation, MixerPref_PointFiltering, MixerPref_RenderTargetMask, MixerPref_RenderTargetRGB, MixerPref_RenderTargetReserved, MixerPref_RenderTargetYUV, MixerPref_RenderTargetYUV420, MixerPref_RenderTargetYUV422, MixerPref_RenderTargetYUV444, VMRMixerPrefs, VMRMixerPrefs enumeration [DirectShow], VMRMixerPrefsEnumeration, dshow.vmrmixerprefs, strmif/MixerPref_ARAdjustXorY, strmif/MixerPref_BiLinearFiltering, strmif/MixerPref_DecimateMask, strmif/MixerPref_DecimateOutput, strmif/MixerPref_DecimationReserved, strmif/MixerPref_DynamicDecimateBy2, strmif/MixerPref_DynamicMask, strmif/MixerPref_DynamicReserved, strmif/MixerPref_DynamicSwitchToBOB, strmif/MixerPref_FilteringMask, strmif/MixerPref_NoDecimation, strmif/MixerPref_PointFiltering, strmif/MixerPref_RenderTargetMask, strmif/MixerPref_RenderTargetRGB, strmif/MixerPref_RenderTargetReserved, strmif/MixerPref_RenderTargetYUV, strmif/MixerPref_RenderTargetYUV420, strmif/MixerPref_RenderTargetYUV422, strmif/MixerPref_RenderTargetYUV444, strmif/VMRMixerPrefs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
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
 - strmif.h
api_name:
 - VMRMixerPrefs
product: Windows
targetos: Windows
req.typenames: VMRMixerPrefs
req.redist: 
---

# VMRMixerPrefs enumeration


## -description



The <b>VMRMixerPrefs</b> enumeration contains flags that specify decimation, filtering, and color space information that will be used when the video image is created on the DirectDraw surface.




## -enum-fields




### -field MixerPref_NoDecimation

No decimation. The video will be rendered onto the surface in its native size.


### -field MixerPref_DecimateOutput

Decimate output by 2 in the x and y directions.


### -field MixerPref_ARAdjustXorY

Adjust the horizontal or vertical size of the video streams to match the target aspect ratio. If this flag is not present, the VMR adjusts the horizontal size only. For more information, see <a href="https://msdn.microsoft.com/0ed6010b-9168-44b1-be49-0c9d5d77ce3f">Aspect Ratio Correction</a>.


### -field MixerPref_DecimationReserved

Reserved.


### -field MixerPref_DecimateMask

Bitmask to isolate the flags that control decimation. (This value is not a valid flag.)


### -field MixerPref_BiLinearFiltering

Use bi-linear filtering. This is the default type of filtering, but not all cards can support it.


### -field MixerPref_PointFiltering

Use point filtering.


### -field MixerPref_FilteringMask

Bitmask to isolate the flags the control filtering. (This value is not a valid flag.)


### -field MixerPref_RenderTargetRGB

The render target is an RGB surface.


### -field MixerPref_RenderTargetYUV

The render target is a YUV surface. Requires Windows XP Service Pack 2. For more information, see <a href="https://msdn.microsoft.com/296b1d96-1824-4000-8bec-158925555177">YUV Mixing Mode</a>.


### -field MixerPref_RenderTargetYUV420

The render target is a YUV 4:2:0 surface. <div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>



### -field MixerPref_RenderTargetYUV422

The render target is a YUV 4:2:2 surface. <div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>



### -field MixerPref_RenderTargetYUV444

The render target is a YUV 4:4:4 surface. <div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>



### -field MixerPref_RenderTargetReserved

Reserved.


### -field MixerPref_RenderTargetMask

Bitmask to isolate flags that control the render target. (This value is not a valid flag.)


### -field MixerPref_DynamicSwitchToBOB

In YUV mixing mode only, this flag switches the VMR to bob deinterlacing. You can add or remove this flag while the filter graph is running; the change will be applied when the VMR mixer composes the next video frame.


### -field MixerPref_DynamicDecimateBy2

In YUV mixing mode only, this flag causes the VMR to decimate the image by a factor of 2 horizontally and vertically. You can add or remove this flag while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.


### -field MixerPref_DynamicReserved

Reserved.


### -field MixerPref_DynamicMask

Bitmask to isolate the MixerPref_DynamicSwitchToBOB and MixerPref_DynamicDecimateBy2 flags. (This value is not a valid flag.)


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/ee410a7e-e021-408a-bf40-cb58dc8eca1c">IVMRMixerControl::GetMixingPrefs</a>



<a href="https://msdn.microsoft.com/e7e1689c-03b4-457e-8d4c-6d59a70c42af">IVMRMixerControl::SetMixingPrefs</a>
 

 

