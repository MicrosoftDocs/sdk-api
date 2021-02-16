---
UID: NS:dxmini._DDSETSTATEOUTINFO
title: DDSETSTATEOUTINFO (dxmini.h)
description: The DDSETSTATEOUTINFO structure contains the state information for the video port extensions (VPE) object.
helpviewer_keywords: ["*PDDSETSTATEOUTINFO","DDSETSTATEOUTINFO","DDSETSTATEOUTINFO structure [Display Devices]","PDDSETSTATEOUTINFO","PDDSETSTATEOUTINFO structure pointer [Display Devices]","Video_Structs_2c99366e-e41f-460b-b8ff-d3173ecc010c.xml","display.ddsetstateoutinfo","dxmini/DDSETSTATEOUTINFO","dxmini/PDDSETSTATEOUTINFO"]
old-location: display\ddsetstateoutinfo.htm
tech.root: display
ms.assetid: 11cd0d5e-6fe2-47eb-a410-0aa7ada30f87
ms.date: 12/05/2018
ms.keywords: '*PDDSETSTATEOUTINFO, DDSETSTATEOUTINFO, DDSETSTATEOUTINFO structure [Display Devices], PDDSETSTATEOUTINFO, PDDSETSTATEOUTINFO structure pointer [Display Devices], Video_Structs_2c99366e-e41f-460b-b8ff-d3173ecc010c.xml, display.ddsetstateoutinfo, dxmini/DDSETSTATEOUTINFO, dxmini/PDDSETSTATEOUTINFO'
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
targetos: Windows
req.typenames: DDSETSTATEOUTINFO, *PDDSETSTATEOUTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSETSTATEOUTINFO
 - dxmini/_DDSETSTATEOUTINFO
 - PDDSETSTATEOUTINFO
 - dxmini/PDDSETSTATEOUTINFO
 - DDSETSTATEOUTINFO
 - dxmini/DDSETSTATEOUTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDSETSTATEOUTINFO
---

# DDSETSTATEOUTINFO structure


## -description

The DDSETSTATEOUTINFO structure contains the state information for the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

## -struct-fields

### -field bSoftwareAutoflip

When set to a nonzero value, causes Microsoft DirectDraw to revert to software autoflipping. Note that once software autoflipping has been initiated, you cannot revert back to hardware autoflipping until the VPE object and surface are destroyed and restarted.

### -field dwSurfaceIndex

Indicates the zero-based index in the autoflip chain of the surface currently receiving the data from the VPE object. This field is ignored unless the miniport driver is switching from hardware autoflipping to software autoflipping.

### -field dwVBISurfaceIndex

Indicates the zero-based index in the autoflip chain of the <a href="/windows-hardware/drivers/">vertical blanking interval (VBI)</a> surface currently receiving the data from the VPE object. This field is ignored unless the video miniport driver is switching from hardware autoflipping to software autoflipping.

## -remarks

When asked to switch from bob to weave, the video miniport driver might need to switch from hardware autoflipping to software autoflipping (no current hardware supports automatic field skipping, and so on). All the driver has to do is set the <b>bSoftwareAutoflip</b> member to a nonzero value and DirectDraw reverts to software autoflipping. 

If the miniport driver switches from hardware to software autoflipping, DirectDraw must know which surface is currently receiving data from the VPE object so it can continue without causing a glitch. Therefore, the miniport driver must set the <b>dwSurfaceIndex</b> member to the index in the autoflip chain of the surface currently receiving the data from the VPE object. When <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a> is called, it gives an array of surfaces that the driver can autoflip between. You can program the addresses of these surfaces that are used for software autoflipping into your hardware.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_setstate">DxSetState</a>