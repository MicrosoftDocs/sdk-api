---
UID: NS:ddrawint._DD_FLIPDATA
title: DD_FLIPDATA (ddrawint.h)
description: The DD_FLIPDATA structure contains information needed to do a flip.
helpviewer_keywords: ["*PDD_FLIPDATA","DD_FLIPDATA","DD_FLIPDATA structure [Display Devices]","ddrawint/DD_FLIPDATA","ddstrcts_cfb79a99-a030-4516-8b9f-b6c01b69187d.xml","display.dd_flipdata"]
old-location: display\dd_flipdata.htm
tech.root: display
ms.assetid: 1926db26-4a29-4ddb-85c6-dd2074eba0b8
ms.date: 12/05/2018
ms.keywords: '*PDD_FLIPDATA, DD_FLIPDATA, DD_FLIPDATA structure [Display Devices], ddrawint/DD_FLIPDATA, ddstrcts_cfb79a99-a030-4516-8b9f-b6c01b69187d.xml, display.dd_flipdata'
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
req.typenames: '*PDD_FLIPDATA, DD_FLIPDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_FLIPDATA
 - ddrawint/_DD_FLIPDATA
 - PDD_FLIPDATA
 - ddrawint/PDD_FLIPDATA
 - DD_FLIPDATA
 - ddrawint/DD_FLIPDATA
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
 - DD_FLIPDATA
---

# DD_FLIPDATA structure


## -description

The DD_FLIPDATA structure contains information needed to do a flip.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpSurfCurr

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure describing the current surface.

### -field lpSurfTarg

Points to the DD_SURFACE_LOCAL structure describing the target surface; that is, the surface to which the driver should flip.

### -field dwFlags

Indicates a set of flags that provide the driver with details for the flip. This member can be a bitwise OR of the following flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDFLIP_DONOTWAIT

</td>
<td>
Specifies to return DDERR_WASSTILLDRAWING if the accelerator is busy. The default is DDFLIP_WAIT.

</td>
</tr>
<tr>
<td>
DDFLIP_EVEN

</td>
<td>
The surface to which the <b>lpSurfTarg</b> member points contains only the even field of video data. This flag is valid only when the surface is an overlay, and is mutually exclusive of DDFLIP_ODD.

</td>
</tr>
<tr>
<td>
DDFLIP_ODD

</td>
<td>
The surface to which the <b>lpSurfTarg</b> member points contains only the odd field of video data. This flag is valid only when the surface is an overlay, and is mutually exclusive of DDFLIP_EVEN.

</td>
</tr>
<tr>
<td>
DDFLIP_NOVSYNC

</td>
<td>
The driver should perform the flip and return immediately. Typically, the current back buffer (which used to be the front buffer) is still visible until the next vertical retrace. Subsequent operations involving the surfaces to which the <b>lpSurfCurr</b> and <b>lpSurfTarg</b> members point do not check to see if the physical flip has finished. This allows an application to perform flips at a higher frequency than the monitor refresh rate, although it might introduce visible artifacts.

</td>
</tr>
<tr>
<td>
DDFLIP_INTERVAL2

</td>
<td>
The driver should perform the flip on every other vertical sync. It should return DDERR_WASSTILLDRAWING until the second vertical retrace has occurred. This flag is mutually exclusive of DDFLIP_INTERVAL3 and DDFLIP_INTERVAL4.

</td>
</tr>
<tr>
<td>
DDFLIP_INTERVAL3

</td>
<td>
The driver should perform the flip on every third vertical sync. It should return DDERR_WASSTILLDRAWING until the third vertical retrace has occurred. This flag is mutually exclusive of DDFLIP_INTERVAL2 and DDFLIP_INTERVAL4.

</td>
</tr>
<tr>
<td>
DDFLIP_INTERVAL4

</td>
<td>
The driver should perform the flip on every fourth vertical sync. It should return DDERR_WASSTILLDRAWING until the fourth vertical retrace has occurred. This flag is mutually exclusive of DDFLIP_INTERVAL2 and DDFLIP_INTERVAL3.

</td>
</tr>
<tr>
<td>
DDFLIP_STEREO

</td>
<td>
Specifies to enable stereo autoflipping (the hardware automatically flips between the left and right buffers during each screen refresh).

</td>
</tr>
<tr>
<td>
DDFLIP_WAIT

</td>
<td>
Specifies to not return until the flip or an error occurs.

</td>
</tr>
</table>

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field Flip

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

### -field lpSurfCurrLeft

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure describing the current left surface.

### -field lpSurfTargLeft

Points to the DD_SURFACE_LOCAL structure describing the left target surface to flip to.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a>