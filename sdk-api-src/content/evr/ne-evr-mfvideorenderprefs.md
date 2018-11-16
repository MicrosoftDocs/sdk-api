---
UID: NE:evr.MFVideoRenderPrefs
title: MFVideoRenderPrefs
author: windows-sdk-content
description: Contains flags that define how the enhanced video renderer (EVR) displays the video.
old-location: mf\mfvideorenderprefs.htm
tech.root: medfound
ms.assetid: a56e7e09-23af-4ad3-9846-4102233ed3c4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MFVideoRenderPrefs, MFVideoRenderPrefs enumeration [Media Foundation], MFVideoRenderPrefs_AllowBatching, MFVideoRenderPrefs_AllowOutputThrottling, MFVideoRenderPrefs_AllowScaling, MFVideoRenderPrefs_DoNotClipToDevice, MFVideoRenderPrefs_DoNotRenderBorder, MFVideoRenderPrefs_DoNotRepaintOnStop, MFVideoRenderPrefs_ForceBatching, MFVideoRenderPrefs_ForceOutputThrottling, MFVideoRenderPrefs_ForceScaling, MFVideoRenderPrefs_Mask, a56e7e09-23af-4ad3-9846-4102233ed3c4, evr/MFVideoRenderPrefs, evr/MFVideoRenderPrefs_AllowBatching, evr/MFVideoRenderPrefs_AllowOutputThrottling, evr/MFVideoRenderPrefs_AllowScaling, evr/MFVideoRenderPrefs_DoNotClipToDevice, evr/MFVideoRenderPrefs_DoNotRenderBorder, evr/MFVideoRenderPrefs_DoNotRepaintOnStop, evr/MFVideoRenderPrefs_ForceBatching, evr/MFVideoRenderPrefs_ForceOutputThrottling, evr/MFVideoRenderPrefs_ForceScaling, evr/MFVideoRenderPrefs_Mask, mf.mfvideorenderprefs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: evr.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr.h
api_name:
 - MFVideoRenderPrefs
product: Windows
targetos: Windows
req.typenames: MFVideoRenderPrefs
req.redist: 
---

# MFVideoRenderPrefs enumeration


## -description



Contains flags that define how the enhanced video renderer (EVR) displays the video.




## -enum-fields




### -field MFVideoRenderPrefs_DoNotRenderBorder

If this flag is set, the EVR does not draw the border color. By default, the EVR draws a border on areas of the destination rectangle that have no video. See <a href="https://msdn.microsoft.com/4a3647a8-4789-4f18-979b-4a9ee1ce7b71">IMFVideoDisplayControl::SetBorderColor</a>.
          


### -field MFVideoRenderPrefs_DoNotClipToDevice

If this flag is set, the EVR does not clip the video when the video window straddles two monitors. By default, if the video window straddles two monitors, the EVR clips the video to the monitor that contains the largest area of video.
          


### -field MFVideoRenderPrefs_AllowOutputThrottling


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Allow the EVR to limit its output to match GPU bandwidth.


### -field MFVideoRenderPrefs_ForceOutputThrottling


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Force the EVR
            to limit its output to match GPU bandwidth.


### -field MFVideoRenderPrefs_ForceBatching


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Force the EVR to batch Direct3D <b>Present</b> calls. This optimization enables the system to enter to idle states more frequently, which can reduce power consumption.
            


### -field MFVideoRenderPrefs_AllowBatching


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Allow the EVR to batch Direct3D <b>Present</b> calls.


### -field MFVideoRenderPrefs_ForceScaling


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Force the EVR to mix the video inside a rectangle that is smaller than the output rectangle. The EVR will then scale the result to the correct output size. The effective resolution will be lower if this setting is applied.


### -field MFVideoRenderPrefs_AllowScaling


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Allow
            the EVR to mix the video inside a rectangle that is smaller than the output rectangle. 


### -field MFVideoRenderPrefs_DoNotRepaintOnStop


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


Prevent the EVR from repainting the video window after a stop command. By default, the EVR repaints the video window black after a stop command.


### -field MFVideoRenderPrefs_Mask

Bitmask to validate flag values. This value is not a valid flag.
          


## -remarks



To set these flags, call <a href="https://msdn.microsoft.com/7603aaf8-1671-4b35-bee5-335f656de3c5">IMFVideoDisplayControl::SetRenderingPrefs</a>.

The flags named "MFVideoRenderPrefs_Allow..." cause the EVR to use lower-quality settings only when requested by the quality manager. (For more information, see <a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>.) The flags named "MFVideoRenderPrefs_Force..." cause the video mixer to use lower-quality settings regardless of the quality manager.






## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

