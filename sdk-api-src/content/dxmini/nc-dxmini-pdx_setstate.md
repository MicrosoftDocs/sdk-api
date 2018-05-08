---
UID: NC:dxmini.PDX_SETSTATE
title: PDX_SETSTATE
author: windows-driver-content
description: The DxSetState callback function is called when a client of the video miniport driver decides it wants to switch from bob mode to weave mode, and vice versa.
old-location: display\dxsetstate.htm
old-project: display
ms.assetid: f2d7f248-017e-4375-b0a0-49de65192511
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: DxSetState, DxSetState callback function [Display Devices], PDX_SETSTATE, PDX_SETSTATE callback, VideoMiniPort_DxApiFunctions_f9872ae5-7be7-4a13-bcb1-01353b3eb793.xml, display.dxsetstate, dxmini/DxSetState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Desktop
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
req.typenames: DXGI_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	dxmini.h
api_name:
-	DxSetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PDX_SETSTATE callback function


## -description


The<i> DxSetState</i> callback function is called when a client of the video miniport driver decides it wants to switch from bob mode to weave mode, and vice versa. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - HwDeviceExtension

Points to the miniport driver's device extension.


#### - SetStateInInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550319">DDSETSTATEININFO</a> structure that contains the surface and VPE object information.


#### - SetStateOutInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550320">DDSETSTATEOUTINFO</a> structure that contains the state information for the hardware video port.


## -returns



<i>DxSetState</i> returns DX_OK if it succeeds; otherwise, it returns one of the following error values:




## -remarks



The surface data passed contains the new state. If the new state is not supported, the video miniport driver should fail the call. 

If the new state requires the device to revert from hardware autoflipping to software autoflipping, the video miniport driver should set members of the DDSETSTATEOUTINFO structure at <i>SetStateOutInfo</i> as follows:

<ul>
<li>
The <b>dwSoftwareAutoflip</b> member equal to 1.

</li>
<li>
The <b>dwSurfaceIndex</b> member equal to the current position in the auto-flip list of the surface receiving hardware video port data.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550319">DDSETSTATEININFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550320">DDSETSTATEOUTINFO</a>
 

 

