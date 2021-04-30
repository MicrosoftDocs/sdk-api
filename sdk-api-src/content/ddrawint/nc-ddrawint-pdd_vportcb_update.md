---
UID: NC:ddrawint.PDD_VPORTCB_UPDATE
title: PDD_VPORTCB_UPDATE (ddrawint.h)
description: The DdVideoPortUpdate callback function starts and stops the VPE object, and modifies the VPE object data stream.
helpviewer_keywords: ["DdVideoPortUpdate","DdVideoPortUpdate callback function [Display Devices]","PDD_VPORTCB_UPDATE","PDD_VPORTCB_UPDATE callback","ddfncs_fd19067f-3bed-443f-a11f-78b740d9e34b.xml","ddrawint/DdVideoPortUpdate","display.ddvideoportupdate"]
old-location: display\ddvideoportupdate.htm
tech.root: display
ms.assetid: 50a55a89-bae0-4a65-96ef-3e9903f45a0c
ms.date: 12/05/2018
ms.keywords: DdVideoPortUpdate, DdVideoPortUpdate callback function [Display Devices], PDD_VPORTCB_UPDATE, PDD_VPORTCB_UPDATE callback, ddfncs_fd19067f-3bed-443f-a11f-78b740d9e34b.xml, ddrawint/DdVideoPortUpdate, display.ddvideoportupdate
req.header: ddrawint.h
req.include-header: Winddi.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_VPORTCB_UPDATE
 - ddrawint/PDD_VPORTCB_UPDATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortUpdate
---

## -description

The <b>DdVideoPortUpdate</b> callback function starts and stops the VPE object, and modifies the VPE object data stream.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_updatevportdata">DD_UPDATEVPORTDATA</a> structure that contains the information required for the driver to update the VPE object.

## -returns

<b>DdVideoPortUpdate</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that support VPE must implement <b>DdVideoPortUpdate</b>.

When the <b>dwFlags</b> member of the DD_UPDATEVPORTDATA structure at <i>lpUpdate</i> is DDRAWI_VPORTSTART or DDRAWI_VPORTUPDATE, the driver should do the following:

<ul>
<li>
Check all flags in the <b>dwVPFlags</b> member of the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportinfo">DDVIDEOPORTINFO</a> structure to which the <i>lpVideoInfo</i> member of DD_UPDATEVPORTDATA points. These flags describe how the driver should transfer video data to a surface (or surfaces); for example, they indicate whether the driver should perform autoflipping, crop the video or <a href="/windows-hardware/drivers/">VBI</a> data, etc.

</li>
<li>
Set up loops in the hardware to write video and/or VBI data to the surfaces in the order in which the surfaces are stored in the array(s). The driver should return as quickly as possible after setting up these loops.

</li>
<li>
If autoflipping has been requested, store the frame buffer offset for each surface in the driver's internal data structure. The surface offsets should be stored in the order in which the surfaces occur in the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_int">DD_SURFACE_INT</a> arrays at the <b>lplpDDSurface</b> and <b>lplpDDVBISurface</b> members of DD_UPDATEVPORTDATA. In this way, when <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a> is called, the driver has a record of the flipping order of the surface chain.

</li>
</ul>
If the <b>dwVBIHeight</b> member of the DDVIDEOPORTINFO structure is greater than zero and <b>lplpDDVBISurface</b> is not <b>NULL</b>, the driver should write the lines of <a href="/windows-hardware/drivers/">VBI</a> data specified by the number in <b>dwVBIHeight</b> into each surface in the array to which <b>lplpDDVBISurface</b> points.

If the driver's hardware cannot support the number of surfaces specified when autoflipping is requested, <b>DdVideoPortUpdate</b> should fail the call by setting DDERR_UNSUPPORTED in the <b>ddRVal</b> member of DD_UPDATEVPORTDATA.

The number of surfaces in the video and <a href="/windows-hardware/drivers/">VBI</a> surface chains can be different; that is, the <b>dwNumAutoflip</b> and <b>dwNumVBIAutoflip</b> members of DD_UPDATEVPORTDATA can be different values.

When <b>dwFlags</b> is DDRAWI_VPORTSTOP, the driver should return immediately. The driver should not poll until the data stream stops.

## -see-also

<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportinfo">DDVIDEOPORTINFO</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_int">DD_SURFACE_INT</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_updatevportdata">DD_UPDATEVPORTDATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a>