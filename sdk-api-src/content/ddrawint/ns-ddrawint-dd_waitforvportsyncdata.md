---
UID: NS:ddrawint._DD_WAITFORVPORTSYNCDATA
title: DD_WAITFORVPORTSYNCDATA (ddrawint.h)
description: The DD_WAITFORVPORTSYNCDATA structure contains the information required for the driver to synchronize the video port extensions (VPE) object.
helpviewer_keywords: ["*PDD_WAITFORVPORTSYNCDATA","DD_WAITFORVPORTSYNCDATA","DD_WAITFORVPORTSYNCDATA structure [Display Devices]","ddrawint/DD_WAITFORVPORTSYNCDATA","ddstrcts_2a571554-4047-4ffd-88d0-cdea5bfeff63.xml","display.dd_waitforvportsyncdata"]
old-location: display\dd_waitforvportsyncdata.htm
tech.root: display
ms.assetid: 903c697e-4fa5-472e-ab5b-7864a326f323
ms.date: 12/05/2018
ms.keywords: '*PDD_WAITFORVPORTSYNCDATA, DD_WAITFORVPORTSYNCDATA, DD_WAITFORVPORTSYNCDATA structure [Display Devices], ddrawint/DD_WAITFORVPORTSYNCDATA, ddstrcts_2a571554-4047-4ffd-88d0-cdea5bfeff63.xml, display.dd_waitforvportsyncdata'
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
req.typenames: '*PDD_WAITFORVPORTSYNCDATA, DD_WAITFORVPORTSYNCDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_WAITFORVPORTSYNCDATA
 - ddrawint/_DD_WAITFORVPORTSYNCDATA
 - PDD_WAITFORVPORTSYNCDATA
 - ddrawint/PDD_WAITFORVPORTSYNCDATA
 - DD_WAITFORVPORTSYNCDATA
 - ddrawint/DD_WAITFORVPORTSYNCDATA
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
 - DD_WAITFORVPORTSYNCDATA
---

# DD_WAITFORVPORTSYNCDATA structure


## -description

The DD_WAITFORVPORTSYNCDATA structure contains the information required for the driver to synchronize the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.

### -field dwFlags

Indicates the condition for which the driver should wait. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPWAIT_BEGIN

</td>
<td>
The driver should return at the beginning of the next V-sync.

</td>
</tr>
<tr>
<td>
DDVPWAIT_END

</td>
<td>
The driver should return at the end of the next/current V-sync.

</td>
</tr>
<tr>
<td>
DDVPWAIT_LINE

</td>
<td>
The driver should return at the beginning of the line specified in <b>dwLine</b>.

</td>
</tr>
</table>

### -field dwLine

Specifies the line number on which the driver should synchronize when <b>dwFlags</b> is DDVPWAIT_LINE. The driver should ignore this member when <b>dwFlags</b> is set to DDVPWAIT_BEGIN or DDVPWAIT_END.

### -field dwTimeOut

Specifies the maximum amount of time the driver should wait, in milliseconds, before timing out.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_waitforsync">DdVideoPortWaitForSync</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field UpdateVideoPort

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_waitforsync">DdVideoPortWaitForSync</a>