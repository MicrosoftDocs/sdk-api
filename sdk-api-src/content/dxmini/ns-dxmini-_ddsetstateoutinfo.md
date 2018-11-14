---
UID: NS:dxmini._DDSETSTATEOUTINFO
title: "_DDSETSTATEOUTINFO"
author: windows-sdk-content
description: The DDSETSTATEOUTINFO structure contains the state information for the video port extensions (VPE) object.
old-location: display\ddsetstateoutinfo.htm
tech.root: display
ms.assetid: 11cd0d5e-6fe2-47eb-a410-0aa7ada30f87
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PDDSETSTATEOUTINFO, DDSETSTATEOUTINFO, DDSETSTATEOUTINFO structure [Display Devices], PDDSETSTATEOUTINFO, PDDSETSTATEOUTINFO structure pointer [Display Devices], Video_Structs_2c99366e-e41f-460b-b8ff-d3173ecc010c.xml, _DDSETSTATEOUTINFO, display.ddsetstateoutinfo, dxmini/DDSETSTATEOUTINFO, dxmini/PDDSETSTATEOUTINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
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
 - dxmini.h
api_name:
 - DDSETSTATEOUTINFO
product: Windows
targetos: Windows
req.typenames: DDSETSTATEOUTINFO, *PDDSETSTATEOUTINFO
req.redist: 
---

# _DDSETSTATEOUTINFO structure


## -description


The DDSETSTATEOUTINFO structure contains the state information for the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


## -struct-fields




### -field bSoftwareAutoflip

When set to a nonzero value, causes Microsoft DirectDraw to revert to software autoflipping. Note that once software autoflipping has been initiated, you cannot revert back to hardware autoflipping until the VPE object and surface are destroyed and restarted. 


### -field dwSurfaceIndex

Indicates the zero-based index in the autoflip chain of the surface currently receiving the data from the VPE object. This field is ignored unless the miniport driver is switching from hardware autoflipping to software autoflipping. 


### -field dwVBISurfaceIndex

Indicates the zero-based index in the autoflip chain of the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">vertical blanking interval (VBI)</a> surface currently receiving the data from the VPE object. This field is ignored unless the video miniport driver is switching from hardware autoflipping to software autoflipping. 


## -remarks



When asked to switch from bob to weave, the video miniport driver might need to switch from hardware autoflipping to software autoflipping (no current hardware supports automatic field skipping, and so on). All the driver has to do is set the <b>bSoftwareAutoflip</b> member to a nonzero value and DirectDraw reverts to software autoflipping. 

If the miniport driver switches from hardware to software autoflipping, DirectDraw must know which surface is currently receiving data from the VPE object so it can continue without causing a glitch. Therefore, the miniport driver must set the <b>dwSurfaceIndex</b> member to the index in the autoflip chain of the surface currently receiving the data from the VPE object. When <a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a> is called, it gives an array of surfaces that the driver can autoflip between. You can program the addresses of these surfaces that are used for software autoflipping into your hardware. 




## -see-also




<a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a>



<a href="https://msdn.microsoft.com/f2d7f248-017e-4375-b0a0-49de65192511">DxSetState</a>
 

 

