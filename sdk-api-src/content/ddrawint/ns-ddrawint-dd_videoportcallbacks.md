---
UID: NS:ddrawint.DD_VIDEOPORTCALLBACKS
title: DD_VIDEOPORTCALLBACKS (ddrawint.h)
description: The DD_VIDEOPORTCALLBACKS structure contains entry pointers to Microsoft DirectDraw video port extensions (VPE) callback functions that a device driver supports.
helpviewer_keywords: ["*PDD_VIDEOPORTCALLBACKS","DD_VIDEOPORTCALLBACKS","DD_VIDEOPORTCALLBACKS structure [Display Devices]","PDD_VIDEOPORTCALLBACKS","PDD_VIDEOPORTCALLBACKS structure pointer [Display Devices]","ddrawint/DD_VIDEOPORTCALLBACKS","ddrawint/PDD_VIDEOPORTCALLBACKS","ddstrcts_e0a55748-eb24-4e5f-8208-bcb0083cdf21.xml","display.dd_videoportcallbacks"]
old-location: display\dd_videoportcallbacks.htm
tech.root: display
ms.assetid: 5e03d240-f483-4ecf-8890-b9f0368e2b2f
ms.date: 12/05/2018
ms.keywords: '*PDD_VIDEOPORTCALLBACKS, DD_VIDEOPORTCALLBACKS, DD_VIDEOPORTCALLBACKS structure [Display Devices], PDD_VIDEOPORTCALLBACKS, PDD_VIDEOPORTCALLBACKS structure pointer [Display Devices], ddrawint/DD_VIDEOPORTCALLBACKS, ddrawint/PDD_VIDEOPORTCALLBACKS, ddstrcts_e0a55748-eb24-4e5f-8208-bcb0083cdf21.xml, display.dd_videoportcallbacks'
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
req.typenames: DD_VIDEOPORTCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_VIDEOPORTCALLBACKS
 - ddrawint/DD_VIDEOPORTCALLBACKS
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
 - DD_VIDEOPORTCALLBACKS
---

# DD_VIDEOPORTCALLBACKS structure


## -description

The DD_VIDEOPORTCALLBACKS structure contains entry pointers to Microsoft DirectDraw <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> callback functions that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_VIDEOPORTCALLBACKS structure.

### -field dwFlags

Indicates what VPE callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_VPORT32_CANCREATEVIDEOPORT</dt>
<dt>DDHAL_VPORT32_CREATEVIDEOPORT</dt>
<dt>DDHAL_VPORT32_FLIP</dt>
<dt>DDHAL_VPORT32_GETBANDWIDTH</dt>
<dt>DDHAL_VPORT32_GETINPUTFORMATS</dt>
<dt>DDHAL_VPORT32_GETOUTPUTFORMATS</dt>
<dt>DDHAL_VPORT32_GETAUTOFLIPSURF</dt>
<dt>DDHAL_VPORT32_GETFIELD</dt>
<dt>DDHAL_VPORT32_GETLINE</dt>
<dt>DDHAL_VPORT32_GETCONNECT</dt>
<dt>DDHAL_VPORT32_DESTROY</dt>
<dt>DDHAL_VPORT32_GETFLIPSTATUS</dt>
<dt>DDHAL_VPORT32_UPDATE</dt>
<dt>DDHAL_VPORT32_WAITFORSYNC</dt>
<dt>DDHAL_VPORT32_GETSIGNALSTATUS</dt>
<dt>DDHAL_VPORT32_COLORCONTROL</dt>
</dl>

### -field CanCreateVideoPort

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_cancreatevideoport">DdVideoPortCanCreate</a> callback.

### -field CreateVideoPort

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_createvideoport">DdVideoPortCreate</a> callback.

### -field FlipVideoPort

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_flip">DdVideoPortFlip</a> callback.

### -field GetVideoPortBandwidth

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a> callback.

### -field GetVideoPortInputFormats

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getinputformats">DdVideoPortGetInputFormats</a> callback.

### -field GetVideoPortOutputFormats

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getoutputformats">DdVideoPortGetOutputFormats</a> callback.

### -field lpReserved1

Reserved for system use and should be ignored by the driver.

### -field GetVideoPortField

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getfield">DdVideoPortGetField</a> callback.

### -field GetVideoPortLine

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getline">DdVideoPortGetLine</a> callback.

### -field GetVideoPortConnectInfo

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getvportconnect">DdVideoPortGetConnectInfo</a> callback.

### -field DestroyVideoPort

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_destroyvport">DdVideoPortDestroy</a> callback.

### -field GetVideoPortFlipStatus

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getflipstatus">DdVideoPortGetFlipStatus</a> callback.

### -field UpdateVideoPort

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a> callback.

### -field WaitForVideoPortSync

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_waitforsync">DdVideoPortWaitForSync</a> callback.

### -field GetVideoSignalStatus

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getsignalstatus">DdVideoPortGetSignalStatus</a> callback.

### -field ColorControl

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_colorcontrol">DdVideoPortColorControl</a> callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_VideoPortCallbacks GUID.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>