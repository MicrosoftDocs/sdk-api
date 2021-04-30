---
UID: NC:ddrawint.PDD_VPORTCB_COLORCONTROL
title: PDD_VPORTCB_COLORCONTROL (ddrawint.h)
description: The DdVideoPortColorControl callback function gets or sets the VPE object color controls.
helpviewer_keywords: ["DdVideoPortColorControl","DdVideoPortColorControl callback function [Display Devices]","PDD_VPORTCB_COLORCONTROL","PDD_VPORTCB_COLORCONTROL callback","ddfncs_42f1c569-d463-4c22-af43-fb4d829843ab.xml","ddrawint/DdVideoPortColorControl","display.ddvideoportcolorcontrol"]
old-location: display\ddvideoportcolorcontrol.htm
tech.root: display
ms.assetid: 0d4d5157-cadf-4b63-aafc-ccb252cec2b4
ms.date: 12/05/2018
ms.keywords: DdVideoPortColorControl, DdVideoPortColorControl callback function [Display Devices], PDD_VPORTCB_COLORCONTROL, PDD_VPORTCB_COLORCONTROL callback, ddfncs_42f1c569-d463-4c22-af43-fb4d829843ab.xml, ddrawint/DdVideoPortColorControl, display.ddvideoportcolorcontrol
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
 - PDD_VPORTCB_COLORCONTROL
 - ddrawint/PDD_VPORTCB_COLORCONTROL
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
 - DdVideoPortColorControl
---

## -description

The <b>DdVideoPortColorControl</b> callback function gets or sets the VPE object color controls.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_vportcolordata">DD_VPORTCOLORDATA</a> structure that contains the information required for the driver to get the current VPE object color controls or to set new values.

## -returns

<b>DdVideoPortColorControl</b> returns one of the following callback codes:

## -remarks

DirectDraw drivers that set the DDVPCAPS_COLORCONTROL flag in the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a> structure must implement <b>DdVideoPortColorControl</b>.

Depending on the value of the <b>dwFlags</b> member of the DD_VPORTCOLORDATA structure at <i>lpColorControl</i>, the driver should do the following:

<ul>
<li>
When <b>dwFlags</b> is DDRAWI_VPORTGETCOLOR, the driver should fill in each member of the <a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a> structure that it supports with the VPE object's current color control setting. The driver must set the corresponding bit in the <b>dwFlags</b> member of DDCOLORCONTROL for every color control member in which it writes data.

<b>DdVideoPortColorControl</b> can be called to determine the color control capabilities of the VPE object. The driver should therefore fail the call if it does not support a requested color control capability.

</li>
<li>
When <b>dwFlags</b> is DDRAWI_VPORTSETCOLOR, the driver should set the VPE object's color control settings to the values specified in the DDCOLORCONTROL structure. The driver should check the <b>dwFlags</b> member of DDCOLORCONTROL to determine which structure members contain valid data.

</li>
</ul>

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a>



<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_vportcolordata">DD_VPORTCOLORDATA</a>