---
UID: NC:winddi.WNDOBJCHANGEPROC
title: WNDOBJCHANGEPROC
description: The **WNDOBJCHANGEPROC** function is a driver-defined callback function that GDI uses to notify the driver of changes to the window in question.
tech.root: display
ms.date: 07/12/2022
helpviewer_keywords:
 - WNDOBJCHANGEPROC
req.construct-type: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
f1_keywords:
 - WNDOBJCHANGEPROC
 - winddi/WNDOBJCHANGEPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winddi.h
api_name:
 - WNDOBJCHANGEPROC
---

## -description

The **WNDOBJCHANGEPROC** function is a driver-defined callback function that GDI uses to notify the driver of changes to the window in question.

## -parameters

### -param pwo

Pointer to a [WNDOBJ](/windows/win32/api/winddi/ns-winddi-wndobj) structure defining the window object that is currently changing. The window object contains the new size and position of the window. If *fl* is **WOC_CHANGED**, then this parameter is **NULL**.

### -param fl

A flag that describes the change occurring to the window object. This parameter can be one of the following values:

  - WOC\_RGN\_CLIENT\_DELTA  
The WNDOBJ contains a delta client region. The delta region is valid for this call only.

  - WOC\_RGN\_CLIENT  
The WNDOBJ contains a new client region.

  - WOC\_RGN\_SURFACE\_DELTA  
The WNDOBJ contains a delta surface region. The **pvConsumer** member of the WNDOBJ structure is zero. The delta region is valid for this call only.

  - WOC\_RGN\_SURFACE  
The WNDOBJ refers to a surface region created by GDI. The **pvConsumer** member of the WNDOBJ structure is zero.

  - WOC\_CHANGED  
All windows have been updated. GDI always notifies the driver at the end of a desktop update.

  - WOC\_DELETE  
The WNDOBJ is being deleted as a result of the deletion of the window.

  - WOC\_DRAWN  
The windows subsystem has completed the screen-to-screen blit calls (screen-to-screen [DrvCopyBits](/windows/win32/api/winddi/nf-winddi-drvcopybits) necessary to update the screen contents to correspond with the window region changes.

  - WOC\_SPRITE\_OVERLAP  
A sprite overlaps with the WNDOBJ area. This parameter is used when a sprite is first moved on top of the WNDOBJ area or immediately after the WNDOBJ is created if it overlaps with a preexisting sprite.

  - WOC\_SPRITE\_NO\_OVERLAP  
Sprites no longer overlap the WNDOBJ area. This parameter is used when all sprites have been moved off the WNDOBJ area, and will be used only if the callback was previously called with WOC\_SPRITE\_OVERLAP.

## -remarks

The *pfn* parameter of the [EngCreateWnd](/windows/win32/api/winddi/nf-winddi-engcreatewnd) function points to this function.

## -see-also

* [WNDOBJ](/windows/win32/api/winddi/ns-winddi-wndobj)
* [DrvCopyBits](/windows/win32/api/winddi/nf-winddi-drvcopybits)
* [EngCreateWnd](/windows/win32/api/winddi/nf-winddi-engcreatewnd)
