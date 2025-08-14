---
UID: NF:winddi.EngMovePointer
title: EngMovePointer function (winddi.h)
description: The EngMovePointer function moves the engine-managed pointer on the device.
helpviewer_keywords: ["EngMovePointer","EngMovePointer function [Display Devices]","display.engmovepointer","gdifncs_2499e137-74e8-4624-8595-65d4fb489973.xml","winddi/EngMovePointer"]
old-location: display\engmovepointer.htm
tech.root: display
ms.assetid: 6f427839-034e-46c3-a3b0-703a003af1e4
ms.date: 12/05/2018
ms.keywords: EngMovePointer, EngMovePointer function [Display Devices], display.engmovepointer, gdifncs_2499e137-74e8-4624-8595-65d4fb489973.xml, winddi/EngMovePointer
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngMovePointer
 - winddi/EngMovePointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngMovePointer
---

# EngMovePointer function


## -description

The <b>EngMovePointer</b> function moves the engine-managed pointer on the device.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the display device surface on which the pointer is to be moved.

### -param x [in]

Specify the x-coordinate on the display where the hot spot of the pointer should be positioned.

A negative <i>x</i> value indicates that the pointer should be removed from the display because drawing is about to occur at its present location. If the pointer has been removed from the display and the <i>x</i> value is nonnegative, the pointer should be restored.

### -param y [in]

Specify the y-coordinate on the display where the hot spot of the pointer should be positioned.

### -param prcl [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure defining an area that bounds all pixels affected by the pointer on the display. The driver should pass the <i>prcl</i> parameter received by its <a href="/windows/desktop/api/winddi/nf-winddi-drvmovepointer">DrvMovePointer</a> function. GDI will not draw in this rectangle without first removing the pointer from the screen. This parameter can be <b>NULL</b>.

## -returns

None

## -remarks

<b>EngMovePointer</b> must not be called while any thread is drawing in the display driver.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvmovepointer">DrvMovePointer</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engsetpointershape">EngSetPointerShape</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>