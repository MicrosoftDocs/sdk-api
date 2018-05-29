---
UID: NS:wingdi.DISPLAYCONFIG_VIDEO_SIGNAL_INFO
title: DISPLAYCONFIG_VIDEO_SIGNAL_INFO
author: windows-sdk-content
description: The DISPLAYCONFIG_VIDEO_SIGNAL_INFO structure contains information about the video signal for a display.
old-location: display\displayconfig_video_signal_info.htm
old-project: display
ms.assetid: 960089fe-dbb7-41a1-af73-0002cfce6da2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CCD_Structures_17b322c2-76a8-4f82-8ee7-c70d3f613d5a.xml, DISPLAYCONFIG_VIDEO_SIGNAL_INFO, DISPLAYCONFIG_VIDEO_SIGNAL_INFO structure [Display Devices], display.displayconfig_video_signal_info, wingdi/DISPLAYCONFIG_VIDEO_SIGNAL_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.typenames: DISPLAYCONFIG_VIDEO_SIGNAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wingdi.h
api_name:
-	DISPLAYCONFIG_VIDEO_SIGNAL_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

