---
UID: NS:dxmini._DXAPI_INTERFACE
title: DXAPI_INTERFACE (dxmini.h)
description: The DXAPI_INTERFACE structure contains the interface callback functions that a video miniport driver implements to support Kernel-Mode Video Transport.
helpviewer_keywords: ["*PDXAPI_INTERFACE","DXAPI_INTERFACE","DXAPI_INTERFACE structure [Display Devices]","PDXAPI_INTERFACE","PDXAPI_INTERFACE structure pointer [Display Devices]","ddstrcts_99854747-7e4c-4a5a-9252-13f56abdffbc.xml","display.dxapi_interface","dxmini/DXAPI_INTERFACE","dxmini/PDXAPI_INTERFACE"]
old-location: display\dxapi_interface.htm
tech.root: display
ms.assetid: 137473ea-4785-4118-86af-a859f69f425f
ms.date: 12/05/2018
ms.keywords: '*PDXAPI_INTERFACE, DXAPI_INTERFACE, DXAPI_INTERFACE structure [Display Devices], PDXAPI_INTERFACE, PDXAPI_INTERFACE structure pointer [Display Devices], ddstrcts_99854747-7e4c-4a5a-9252-13f56abdffbc.xml, display.dxapi_interface, dxmini/DXAPI_INTERFACE, dxmini/PDXAPI_INTERFACE'
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DXAPI_INTERFACE, *PDXAPI_INTERFACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXAPI_INTERFACE
 - dxmini/_DXAPI_INTERFACE
 - PDXAPI_INTERFACE
 - dxmini/PDXAPI_INTERFACE
 - DXAPI_INTERFACE
 - dxmini/DXAPI_INTERFACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DXAPI_INTERFACE
---

# DXAPI_INTERFACE structure


## -description

The DXAPI_INTERFACE structure contains the interface callback functions that a <a href="/windows-hardware/drivers/display/video-miniport-drivers-in-the-windows-2000-display-driver-model">video miniport driver</a> implements to support <a href="/windows-hardware/drivers/display/kernel-mode-video-transport">Kernel-Mode Video Transport</a>.

## -struct-fields

### -field Size

Specifies the size in bytes of this DXAPI_INTERFACE structure.

### -field Version

Specifies the version of the video miniport driver's <a href="/windows-hardware/drivers/ddi/content/index">DxApi interface</a>. This value is DXAPI_HALVERSION defined in <i>dxmini.h</i>.

### -field Context

Points to the device extension of the device.

### -field InterfaceReference

Unused by the driver.

### -field InterfaceDereference

Unused by the driver.

### -field DxGetIrqInfo

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getirqinfo">DxGetIRQInfo</a> miniport driver callback function.

### -field DxEnableIrq

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_enableirq">DxEnableIRQ</a> miniport driver callback function.

### -field DxSkipNextField

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_skipnextfield">DxSkipNextField</a> miniport driver callback function.

### -field DxBobNextField

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_bobnextfield">DxBobNextField</a> miniport driver callback function.

### -field DxSetState

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_setstate">DxSetState</a> miniport driver callback function.

### -field DxLock

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_lock">DxLock</a> miniport driver callback function.

### -field DxFlipOverlay

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipoverlay">DxFlipOverlay</a> miniport driver callback function.

### -field DxFlipVideoPort

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_flipvideoport">DxFlipVideoPort</a> miniport driver callback function.

### -field DxGetPolarity

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getpolarity">DxGetPolarity</a> miniport driver callback function.

### -field DxGetCurrentAutoflip

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getcurrentautoflip">DxGetCurrentAutoflip</a> miniport driver callback function.

### -field DxGetPreviousAutoflip

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getpreviousautoflip">DxGetPreviousAutoflip</a> miniport driver callback function.

### -field DxTransfer

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_transfer">DxTransfer</a> miniport driver callback function.

### -field DxGetTransferStatus

Points to the driver-supplied <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_gettransferstatus">DxGetTransferStatus</a> miniport driver callback function.

## -see-also

<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>