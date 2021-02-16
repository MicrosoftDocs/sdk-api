---
UID: NS:ddrawint._DD_VPORTCOLORDATA
title: DD_VPORTCOLORDATA (ddrawint.h)
description: The DD_VPORTCOLORDATA structure contains the video port extensions (VPE) object color control information.
helpviewer_keywords: ["*PDD_VPORTCOLORDATA","DD_VPORTCOLORDATA","DD_VPORTCOLORDATA structure [Display Devices]","ddrawint/DD_VPORTCOLORDATA","ddstrcts_8dc16578-631f-406e-94da-510e6f8b1e24.xml","display.dd_vportcolordata"]
old-location: display\dd_vportcolordata.htm
tech.root: display
ms.assetid: b52bbd7e-2c80-4cfb-b0c5-7900993f4a3a
ms.date: 12/05/2018
ms.keywords: '*PDD_VPORTCOLORDATA, DD_VPORTCOLORDATA, DD_VPORTCOLORDATA structure [Display Devices], ddrawint/DD_VPORTCOLORDATA, ddstrcts_8dc16578-631f-406e-94da-510e6f8b1e24.xml, display.dd_vportcolordata'
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.typenames: '*PDD_VPORTCOLORDATA, DD_VPORTCOLORDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_VPORTCOLORDATA
 - ddrawint/_DD_VPORTCOLORDATA
 - PDD_VPORTCOLORDATA
 - ddrawint/PDD_VPORTCOLORDATA
 - DD_VPORTCOLORDATA
 - ddrawint/DD_VPORTCOLORDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_VPORTCOLORDATA
---

# DD_VPORTCOLORDATA structure


## -description

The DD_VPORTCOLORDATA structure contains the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object color control information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.

### -field dwFlags

Specifies the color control operation to be performed by the driver. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDRAWI_VPORTGETCOLOR

</td>
<td>
The driver should write the current VPE object color controls into the DDCOLORCONTROL structure to which <b>lpColorData</b> points.

</td>
</tr>
<tr>
<td>
DDRAWI_VPORTSETCOLOR

</td>
<td>
The driver should set new values for the VPE object color controls based on the contents of the DDCOLORCONTROL structure to which <b>lpColorData</b> points.

</td>
</tr>
</table>

### -field lpColorData

Points to a <a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a> structure that defines the color control associated with the VPE object to which <b>lpVideoPort</b> points. The value of <b>dwFlags</b> determines whether the driver reads from or writes to this structure.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_colorcontrol">DdVideoPortColorControl</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field ColorControl

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_colorcontrol">DdVideoPortColorControl</a>