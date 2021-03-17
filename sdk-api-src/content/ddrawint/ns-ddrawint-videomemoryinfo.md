---
UID: NS:ddrawint._VIDEOMEMORYINFO
title: VIDEOMEMORYINFO (ddrawint.h)
description: The VIDEOMEMORYINFO structure describes the general format of the display's memory.
helpviewer_keywords: ["*LPVIDEOMEMORYINFO","LPVIDEOMEMORYINFO","LPVIDEOMEMORYINFO structure pointer [Display Devices]","VIDEOMEMORYINFO","VIDEOMEMORYINFO structure [Display Devices]","ddrawint/LPVIDEOMEMORYINFO","ddrawint/VIDEOMEMORYINFO","ddstrcts_7fe9cc27-40d0-41f7-b225-51cc97bc8fa0.xml","display.videomemoryinfo"]
old-location: display\videomemoryinfo.htm
tech.root: display
ms.assetid: c5df8f26-3eb1-4743-96d1-7b73d902be8d
ms.date: 12/05/2018
ms.keywords: '*LPVIDEOMEMORYINFO, LPVIDEOMEMORYINFO, LPVIDEOMEMORYINFO structure pointer [Display Devices], VIDEOMEMORYINFO, VIDEOMEMORYINFO structure [Display Devices], ddrawint/LPVIDEOMEMORYINFO, ddrawint/VIDEOMEMORYINFO, ddstrcts_7fe9cc27-40d0-41f7-b225-51cc97bc8fa0.xml, display.videomemoryinfo'
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
req.typenames: VIDEOMEMORYINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VIDEOMEMORYINFO
 - ddrawint/_VIDEOMEMORYINFO
 - VIDEOMEMORYINFO
 - ddrawint/VIDEOMEMORYINFO
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
 - VIDEOMEMORYINFO
---

## -description

The VIDEOMEMORYINFO structure describes the general format of the display's memory.

## -struct-fields

### -field fpPrimary

Specifies the offset, in bytes, in display memory to the primary surface.

### -field dwFlags

Currently unused and should be set to zero.

### -field dwDisplayWidth

Specifies the current width of the display, in pixels.

### -field dwDisplayHeight

Specifies the current height of the display, in pixels.

### -field lDisplayPitch

Specifies the current pitch of the display, in bytes.

### -field ddpfDisplay

Specifies a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure in which the pixel format of the display is described.

### -field dwOffscreenAlign

Specifies the byte alignment, in bytes, required when allocating this memory for offscreen surfaces.

### -field dwOverlayAlign

Specifies the byte alignment, in bytes, required when allocating this memory for overlay planes.

### -field dwTextureAlign

Specifies the byte alignment, in bytes, required when allocating this memory for textures.

### -field dwZBufferAlign

Specifies the byte alignment, in bytes, required when allocating this memory for the depth buffer.

### -field dwAlphaAlign

Specifies the byte alignment, in bytes, required when allocating this memory for an alpha buffer.

### -field pvPrimary

(Microsoft Windows 2000 and later only) 

Specifies a kernel-mode pointer to the beginning of the primary surface. 

## -remarks

The VIDEOMEMORYINFO structure has minor differences between Windows 98/Me and Windows 2000 and later. On Windows 2000 and later the data structure is called VIDEOMEMORYINFO and on Windows 98/Me the data structure is called VIDMEMINFO. On Windows 2000 and later, VIDEOMEMORYINFO includes a field <b>pvPrimary</b> that stores a kernel-mode pointer to the primary surface. On Windows 98/Me, VIDMEMINFO includes the fields <b>dwNumHeaps</b> and <b>pvmList</b> that specify an array of memory heaps.

GDI allocates memory for and passes a VIDEOMEMORYINFO structure to the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a> function as a member of the DD_HALINFO parameter. The driver should fill in the appropriate members to describe the general characteristics of the device's memory.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a>