---
UID: NS:ddrawint.DD_MOTIONCOMPCALLBACKS
title: DD_MOTIONCOMPCALLBACKS (ddrawint.h)
description: The DD_MOTIONCOMPCALLBACKS structure contains entry pointers to the motion compensation callback functions that a device driver supports.
helpviewer_keywords: ["*PDD_MOTIONCOMPCALLBACKS","DD_MOTIONCOMPCALLBACKS","DD_MOTIONCOMPCALLBACKS structure [Display Devices]","PDD_MOTIONCOMPCALLBACKS","PDD_MOTIONCOMPCALLBACKS structure pointer [Display Devices]","ddrawint/DD_MOTIONCOMPCALLBACKS","ddrawint/PDD_MOTIONCOMPCALLBACKS","ddstrcts_b9c5a52b-5814-42ae-8002-0de8f7c0bca5.xml","display.dd_motioncompcallbacks"]
old-location: display\dd_motioncompcallbacks.htm
tech.root: display
ms.assetid: db707fd8-2190-4c4f-89fd-ab46d97f66a2
ms.date: 12/05/2018
ms.keywords: '*PDD_MOTIONCOMPCALLBACKS, DD_MOTIONCOMPCALLBACKS, DD_MOTIONCOMPCALLBACKS structure [Display Devices], PDD_MOTIONCOMPCALLBACKS, PDD_MOTIONCOMPCALLBACKS structure pointer [Display Devices], ddrawint/DD_MOTIONCOMPCALLBACKS, ddrawint/PDD_MOTIONCOMPCALLBACKS, ddstrcts_b9c5a52b-5814-42ae-8002-0de8f7c0bca5.xml, display.dd_motioncompcallbacks'
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
req.typenames: DD_MOTIONCOMPCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_MOTIONCOMPCALLBACKS
 - ddrawint/DD_MOTIONCOMPCALLBACKS
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
 - DD_MOTIONCOMPCALLBACKS
---

# DD_MOTIONCOMPCALLBACKS structure


## -description

The DD_MOTIONCOMPCALLBACKS structure contains entry pointers to the motion compensation callback functions that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_MOTIONCOMPCALLBACKS structure.

### -field dwFlags

Indicates what additional Microsoft DirectDraw motion compensation callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_MOCOMP32_BEGINFRAME</dt>
<dt>DDHAL_MOCOMP32_CREATE</dt>
<dt>DDHAL_MOCOMP32_DESTROY</dt>
<dt>DDHAL_MOCOMP32_GETCOMPBUFFINFO</dt>
<dt>DDHAL_MOCOMP32_GETINTERNALINFO</dt>
<dt>DDHAL_MOCOMP32_ENDFRAME</dt>
<dt>DDHAL_MOCOMP32_GETFORMATS</dt>
<dt>DDHAL_MOCOMP32_GETGUIDS</dt>
<dt>DDHAL_MOCOMP32_QUERYSTATUS</dt>
<dt>DDHAL_MOCOMP32_RENDER</dt>
</dl>

### -field GetMoCompGuids

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getguids">DdMoCompGetGuids</a> callback function.

### -field GetMoCompFormats

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getformats">DdMoCompGetFormats</a> callback function.

### -field CreateMoComp

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_create">DdMoCompCreate</a> callback function.

### -field GetMoCompBuffInfo

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getcompbuffinfo">DdMoCompGetBuffInfo</a> callback function.

### -field GetInternalMoCompInfo

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getinternalinfo">DdMoCompGetInternalInfo</a> callback function.

### -field BeginMoCompFrame

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_beginframe">DdMoCompBeginFrame</a> callback function.

### -field EndMoCompFrame

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_endframe">DdMoCompEndFrame</a> callback function.

### -field RenderMoComp

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_render">DdMoCompRender</a> callback function.

### -field QueryMoCompStatus

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_querystatus">DdMoCompQueryStatus</a> callback function.

### -field DestroyMoComp

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_destroy">DdMoCompDestroy</a> callback function.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_MotionCompCallbacks GUID.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_beginframe">DdMoCompBeginFrame</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_create">DdMoCompCreate</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_destroy">DdMoCompDestroy</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_endframe">DdMoCompEndFrame</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getcompbuffinfo">DdMoCompGetBuffInfo</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getformats">DdMoCompGetFormats</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getguids">DdMoCompGetGuids</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getinternalinfo">DdMoCompGetInternalInfo</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_querystatus">DdMoCompQueryStatus</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_render">DdMoCompRender</a>