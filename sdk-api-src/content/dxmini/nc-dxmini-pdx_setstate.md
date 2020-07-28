---
UID: NC:dxmini.PDX_SETSTATE
title: PDX_SETSTATE (dxmini.h)
description: The DxSetState callback function is called when a client of the video miniport driver decides it wants to switch from bob mode to weave mode, and vice versa.
helpviewer_keywords: ["DxSetState","DxSetState callback function [Display Devices]","PDX_SETSTATE","PDX_SETSTATE callback","VideoMiniPort_DxApiFunctions_f9872ae5-7be7-4a13-bcb1-01353b3eb793.xml","display.dxsetstate","dxmini/DxSetState"]
old-location: display\dxsetstate.htm
tech.root: display
ms.assetid: f2d7f248-017e-4375-b0a0-49de65192511
ms.date: 12/05/2018
ms.keywords: DxSetState, DxSetState callback function [Display Devices], PDX_SETSTATE, PDX_SETSTATE callback, VideoMiniPort_DxApiFunctions_f9872ae5-7be7-4a13-bcb1-01353b3eb793.xml, display.dxsetstate, dxmini/DxSetState
f1_keywords:
- dxmini/DxSetState
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- dxmini.h
api_name:
- DxSetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddsetstateininfo">DDSETSTATEININFO</a> structure that contains the surface and VPE object information.


#### - SetStateOutInfo

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddsetstateoutinfo">DDSETSTATEOUTINFO</a> structure that contains the state information for the hardware video port.


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




<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddsetstateininfo">DDSETSTATEININFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddsetstateoutinfo">DDSETSTATEOUTINFO</a>
 

 

