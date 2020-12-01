---
UID: NS:ddrawint._DD_GETVPORTOUTPUTFORMATDATA
title: DD_GETVPORTOUTPUTFORMATDATA (ddrawint.h)
description: The DD_GETVPORTOUTPUTFORMATDATA structure contains the information required for the driver to return all of the output formats that the video port extensions (VPE) object supports for a given input format.
helpviewer_keywords: ["*PDD_GETVPORTOUTPUTFORMATDATA","DD_GETVPORTOUTPUTFORMATDATA","DD_GETVPORTOUTPUTFORMATDATA structure [Display Devices]","ddrawint/DD_GETVPORTOUTPUTFORMATDATA","ddstrcts_c8b41b3c-cb15-46d2-aa72-f59301276ffe.xml","display.dd_getvportoutputformatdata"]
old-location: display\dd_getvportoutputformatdata.htm
tech.root: display
ms.assetid: 3033a4e9-3f94-4702-9db8-098a358ab1c2
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTOUTPUTFORMATDATA, DD_GETVPORTOUTPUTFORMATDATA, DD_GETVPORTOUTPUTFORMATDATA structure [Display Devices], ddrawint/DD_GETVPORTOUTPUTFORMATDATA, ddstrcts_c8b41b3c-cb15-46d2-aa72-f59301276ffe.xml, display.dd_getvportoutputformatdata'
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
req.typenames: '*PDD_GETVPORTOUTPUTFORMATDATA, DD_GETVPORTOUTPUTFORMATDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTOUTPUTFORMATDATA
 - ddrawint/_DD_GETVPORTOUTPUTFORMATDATA
 - PDD_GETVPORTOUTPUTFORMATDATA
 - ddrawint/PDD_GETVPORTOUTPUTFORMATDATA
 - DD_GETVPORTOUTPUTFORMATDATA
 - ddrawint/DD_GETVPORTOUTPUTFORMATDATA
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
 - DD_GETVPORTOUTPUTFORMATDATA
---

# DD_GETVPORTOUTPUTFORMATDATA structure


## -description

The DD_GETVPORTOUTPUTFORMATDATA structure contains the information required for the driver to return all of the output formats that the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object supports for a given input format.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.

### -field dwFlags

Indicates the type of output formats for which support is being queried. This member can be one or more of the following values:

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

### -field lpddpfInputFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains an input format supported by the VPE object. This format was returned by <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getinputformats">DdVideoPortGetInputFormats</a>.

### -field lpddpfOutputFormats

Points to an array of DDPIXELFORMAT structures in which the driver should return the output formats that the VPE object supports for the input format specified by <b>lpddpfInputFormat</b>. This member can be <b>NULL</b>.

### -field dwNumFormats

Specifies the location in which the driver should return the number of output formats that the VPE object supports for the specified input format.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getoutputformats">DdVideoPortGetOutputFormats</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortInputFormats

Unused: Win95 compatibility

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getoutputformats">DdVideoPortGetOutputFormats</a>