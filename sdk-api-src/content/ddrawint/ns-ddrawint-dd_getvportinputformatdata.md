---
UID: NS:ddrawint._DD_GETVPORTINPUTFORMATDATA
title: DD_GETVPORTINPUTFORMATDATA (ddrawint.h)
description: The DD_GETVPORTINPUTFORMATDATA structure contains the information required for the driver to return the input formats that the video port extensions (VPE) object can accept.
helpviewer_keywords: ["*PDD_GETVPORTINPUTFORMATDATA","DD_GETVPORTINPUTFORMATDATA","DD_GETVPORTINPUTFORMATDATA structure [Display Devices]","ddrawint/DD_GETVPORTINPUTFORMATDATA","ddstrcts_c9ca2266-9add-4320-8b29-51d67b121957.xml","display.dd_getvportinputformatdata"]
old-location: display\dd_getvportinputformatdata.htm
tech.root: display
ms.assetid: d8cdfb24-0914-4e1f-bbdd-7bba31976ba0
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTINPUTFORMATDATA, DD_GETVPORTINPUTFORMATDATA, DD_GETVPORTINPUTFORMATDATA structure [Display Devices], ddrawint/DD_GETVPORTINPUTFORMATDATA, ddstrcts_c9ca2266-9add-4320-8b29-51d67b121957.xml, display.dd_getvportinputformatdata'
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
req.typenames: '*PDD_GETVPORTINPUTFORMATDATA, DD_GETVPORTINPUTFORMATDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTINPUTFORMATDATA
 - ddrawint/_DD_GETVPORTINPUTFORMATDATA
 - PDD_GETVPORTINPUTFORMATDATA
 - ddrawint/PDD_GETVPORTINPUTFORMATDATA
 - DD_GETVPORTINPUTFORMATDATA
 - ddrawint/DD_GETVPORTINPUTFORMATDATA
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
 - DD_GETVPORTINPUTFORMATDATA
---

# DD_GETVPORTINPUTFORMATDATA structure


## -description

The DD_GETVPORTINPUTFORMATDATA structure contains the information required for the driver to return the input formats that the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object can accept.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.

### -field dwFlags

Indicates the type of formats for which support is being queried. This member can be one or more of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPFORMAT_VBI

</td>
<td>
The driver should return formats for the <a href="/windows-hardware/drivers/">VBI</a> data.

</td>
</tr>
<tr>
<td>
DDVPFORMAT_VIDEO

</td>
<td>
The driver should return formats for the video data.

</td>
</tr>
</table>

### -field lpddpfFormat

Points to an array of <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structures in which the driver should write the pixel formats supported by the VPE object. This member can be <b>NULL</b>.

### -field dwNumFormats

Specifies the location in which the driver should write the number of formats that the VPE object supports.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getinputformats">DdVideoPortGetInputFormats</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortInputFormats

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getinputformats">DdVideoPortGetInputFormats</a>