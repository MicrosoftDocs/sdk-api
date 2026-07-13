---
UID: NF:dmemmgr.HeapVidMemAllocAligned
title: HeapVidMemAllocAligned function (dmemmgr.h)
description: The HeapVidMemAllocAligned function allocates off_screen_memory for a display driver by using the DirectDraw video memory heap manager.
helpviewer_keywords: ["HeapVidMemAllocAligned","HeapVidMemAllocAligned function [Display Devices]","display.heapvidmemallocaligned","dmemmgr/HeapVidMemAllocAligned","gdifncs_07c83436-71a7-4b41-91b9-5b24b6390474.xml"]
old-location: display\heapvidmemallocaligned.htm
tech.root: display
ms.assetid: efd004d5-58fc-4721-9a74-d018cb3e5de9
ms.date: 12/05/2018
ms.keywords: HeapVidMemAllocAligned, HeapVidMemAllocAligned function [Display Devices], display.heapvidmemallocaligned, dmemmgr/HeapVidMemAllocAligned, gdifncs_07c83436-71a7-4b41-91b9-5b24b6390474.xml
req.header: dmemmgr.h
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
 - HeapVidMemAllocAligned
 - dmemmgr/HeapVidMemAllocAligned
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
 - HeapVidMemAllocAligned
---

# HeapVidMemAllocAligned function


## -description

The <b>HeapVidMemAllocAligned</b> function allocates <a href="/windows-hardware/drivers/">off_screen_memory</a> for a display driver by using the DirectDraw video memory heap manager.

## -parameters

### -param lpVidMem [in]

Pointer to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a> structure that represents the DirectDraw heap from which to allocate the surface.

### -param dwWidth [in]

Is the width in bytes of the requested surface.

### -param dwHeight [in]

Is the height in scan lines of the requested surface.

### -param lpAlignment [in]

Pointer to a <a href="/windows/desktop/api/dmemmgr/ns-dmemmgr-surfacealignment">SURFACEALIGNMENT</a> structure that describes the alignment restrictions for the surface.

### -param lpNewPitch [out]

Is the location in which the resulting pitch value is written. This information is relevant only to linear (nonrectangular) off-screen heaps.

## -returns

<b>HeapVidMemAllocAligned</b> returns the FLATPTR offset of the resulting allocation upon success. Otherwise, it returns zero.

## -remarks

The driver should use the array of VIDEOMEMORY structures its <a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a> function receives to determine the value of <i>lpVidMem</i> with which to call <b>HeapVidMemAllocAligned</b>. The driver receives this array in the <i>pvmList</i> parameter during the second call to <b>DrvGetDirectDrawInfo</b>. It is possible that <b>DrvGetDirectDrawInfo</b> might not be called when low memory conditions exist on the system. Consequently, the driver should always check to ensure that it has a non-NULL pointer in <i>pvmList</i>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a>



<a href="/windows/desktop/api/dmemmgr/ns-dmemmgr-surfacealignment">SURFACEALIGNMENT</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a>



<a href="/windows/desktop/api/dmemmgr/nf-dmemmgr-vidmemfree">VidMemFree</a>