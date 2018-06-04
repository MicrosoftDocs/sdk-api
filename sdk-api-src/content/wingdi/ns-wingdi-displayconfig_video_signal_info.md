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

# DISPLAYCONFIG_VIDEO_SIGNAL_INFO structure


## -description


The DISPLAYCONFIG_VIDEO_SIGNAL_INFO structure contains information about the video signal for a display.


## -struct-fields




### -field pixelRate

The pixel clock rate. 


### -field hSyncFreq

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553968">DISPLAYCONFIG_RATIONAL</a> structure that represents horizontal sync.


### -field vSyncFreq

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553968">DISPLAYCONFIG_RATIONAL</a> structure that represents vertical sync. 


### -field activeSize

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553913">DISPLAYCONFIG_2DREGION</a> structure that specifies the width and height (in pixels) of the active portion of the video signal.


### -field totalSize

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553913">DISPLAYCONFIG_2DREGION</a> structure that specifies the width and height (in pixels) of the entire video signal.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.AdditionalSignalInfo

Supported by WDDM 1.3 and later display miniport drivers running on Windows 8.1 and later.


### -field DUMMYUNIONNAME.AdditionalSignalInfo.videoStandard

The video standard (if any) that defines the video signal. For a list of possible values, see the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff546632">D3DKMDT_VIDEO_SIGNAL_STANDARD</a> enumerated type.

Supported starting with Windows 8.1.


### -field DUMMYUNIONNAME.AdditionalSignalInfo.vSyncFreqDivider

The ratio of the VSync rate of a monitor that displays through a Miracast connected session to the VSync rate of the Miracast sink.

To avoid visual artifacts, the VSync rate of the display monitor that's connected to the Miracast sink must be an integer multiple of the VSync rate of the Miracast sink. The display miniport driver reports the latter rate to the operating system as the refresh rate of the desktop present path.

<div class="alert"><b>Note</b>  The operating system fails any attempt by the driver to add a target mode that results in a Miracast target having a VSync rate below 23.9 Hz.</div>
<div> </div>
For a non-Miracast target, the driver should set <b>vSyncFreqDivider</b> to zero.

Supported starting with Windows 8.1.


### -field DUMMYUNIONNAME.AdditionalSignalInfo.reserved

Reserved for system use. Do not use in your driver.

Supported starting with Windows 8.1.


### -field DUMMYUNIONNAME.videoStandard

The video standard (if any) that defines the video signal. For a list of possible values, see the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff546632">D3DKMDT_VIDEO_SIGNAL_STANDARD</a> enumerated type.


### -field scanLineOrdering

The scan-line ordering (for example, progressive or interlaced) of the video signal. For a list of possible values, see the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553977">DISPLAYCONFIG_SCANLINE_ORDERING</a> enumerated type.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546632">D3DKMDT_VIDEO_SIGNAL_STANDARD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553913">DISPLAYCONFIG_2DREGION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553968">DISPLAYCONFIG_RATIONAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553977">DISPLAYCONFIG_SCANLINE_ORDERING</a>
 

 

