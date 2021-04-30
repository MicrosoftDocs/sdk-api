---
UID: NS:winuser.tagPAINTSTRUCT
title: PAINTSTRUCT (winuser.h)
description: The PAINTSTRUCT structure contains information for an application. This information can be used to paint the client area of a window owned by that application.
helpviewer_keywords: ["*LPPAINTSTRUCT","*NPPAINTSTRUCT","*PPAINTSTRUCT","PAINTSTRUCT","PAINTSTRUCT structure [Windows GDI]","PPAINTSTRUCT","PPAINTSTRUCT structure pointer [Windows GDI]","_win32_PAINTSTRUCT_str","gdi.paintstruct","tagPAINTSTRUCT","winuser/PAINTSTRUCT","winuser/PPAINTSTRUCT"]
old-location: gdi\paintstruct.htm
tech.root: gdi
ms.assetid: 1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433
ms.date: 12/05/2018
ms.keywords: '*LPPAINTSTRUCT, *NPPAINTSTRUCT, *PPAINTSTRUCT, PAINTSTRUCT, PAINTSTRUCT structure [Windows GDI], PPAINTSTRUCT, PPAINTSTRUCT structure pointer [Windows GDI], _win32_PAINTSTRUCT_str, gdi.paintstruct, tagPAINTSTRUCT, winuser/PAINTSTRUCT, winuser/PPAINTSTRUCT'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PAINTSTRUCT, *PPAINTSTRUCT, *NPPAINTSTRUCT, *LPPAINTSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPAINTSTRUCT
 - winuser/tagPAINTSTRUCT
 - PPAINTSTRUCT
 - winuser/PPAINTSTRUCT
 - PAINTSTRUCT
 - winuser/PAINTSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - PAINTSTRUCT
---

# PAINTSTRUCT structure


## -description

The <b>PAINTSTRUCT</b> structure contains information for an application. This information can be used to paint the client area of a window owned by that application.

## -struct-fields

### -field hdc

A handle to the display DC to be used for painting.

### -field fErase

Indicates whether the background must be erased. This value is nonzero if the application should erase the background. The application is responsible for erasing the background if a window class is created without a background brush. For more information, see the description of the <b>hbrBackground</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> structure.

### -field rcPaint

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the upper left and lower right corners of the rectangle in which the painting is requested, in device units relative to the upper-left corner of the client area.

### -field fRestore

Reserved; used internally by the system.

### -field fIncUpdate

Reserved; used internally by the system.

### -field rgbReserved

Reserved; used internally by the system.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/gdi/painting-and-drawing-structures">Painting and Drawing Structures</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a>