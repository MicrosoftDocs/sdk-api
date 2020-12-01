---
UID: NS:ddrawint._DD_GETVPORTBANDWIDTHDATA
title: DD_GETVPORTBANDWIDTHDATA (ddrawint.h)
description: The DD_GETVPORTBANDWIDTHDATA structure contains the bandwidth information for any specified format.
helpviewer_keywords: ["*PDD_GETVPORTBANDWIDTHDATA","DD_GETVPORTBANDWIDTHDATA","DD_GETVPORTBANDWIDTHDATA structure [Display Devices]","ddrawint/DD_GETVPORTBANDWIDTHDATA","ddstrcts_3f17b83b-7530-4d17-b6c8-435d9ee45848.xml","display.dd_getvportbandwidthdata"]
old-location: display\dd_getvportbandwidthdata.htm
tech.root: display
ms.assetid: 5a24d819-1498-448a-9360-c14d382059cb
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTBANDWIDTHDATA, DD_GETVPORTBANDWIDTHDATA, DD_GETVPORTBANDWIDTHDATA structure [Display Devices], ddrawint/DD_GETVPORTBANDWIDTHDATA, ddstrcts_3f17b83b-7530-4d17-b6c8-435d9ee45848.xml, display.dd_getvportbandwidthdata'
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
req.typenames: '*PDD_GETVPORTBANDWIDTHDATA, DD_GETVPORTBANDWIDTHDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTBANDWIDTHDATA
 - ddrawint/_DD_GETVPORTBANDWIDTHDATA
 - PDD_GETVPORTBANDWIDTHDATA
 - ddrawint/PDD_GETVPORTBANDWIDTHDATA
 - DD_GETVPORTBANDWIDTHDATA
 - ddrawint/DD_GETVPORTBANDWIDTHDATA
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
 - DD_GETVPORTBANDWIDTHDATA
---

# DD_GETVPORTBANDWIDTHDATA structure


## -description

The DD_GETVPORTBANDWIDTHDATA structure contains the bandwidth information for any specified format.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

### -field lpddpfFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that describes the output pixel format for which the driver should return bandwidth information.

### -field dwWidth

### -field dwHeight

Specify the dimensions of the source overlay or of the video data in pixels depending on the value of <b>dwFlags</b>. These values are calculated by the client based on the VPE object's capabilities returned in a prior call to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>.

### -field dwFlags

Specifies the flags indicating how the driver should interpret the <b>dwWidth</b> and <b>dwHeight</b> members. This member can be one of the values listed in the following table.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPB_OVERLAY

</td>
<td>
The <b>dwWidth</b> and <b>dwHeight</b> members specify the size in pixels of the source overlay surface. This flag indicates that the VPE object is dependent on the overlay source size.

</td>
</tr>
<tr>
<td>
DDVPB_TYPE

</td>
<td>
The <b>dwWidth</b> and <b>dwHeight</b> members are not set.

</td>
</tr>
<tr>
<td>
DDVPB_VIDEOPORT

</td>
<td>
The <b>dwWidth</b> and <b>dwHeight</b> members specify the prescale size of the video data that the VPE object writes to the frame buffer. This flag indicates that the VPE object is dependent on the overlay stretch factor.

</td>
</tr>
</table>

### -field lpBandwidth

Points to the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportbandwidth">DDVIDEOPORTBANDWIDTH</a> structure in which the driver should write the bandwidth parameters.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortBandwidth

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportbandwidth">DDVIDEOPORTBANDWIDTH</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>