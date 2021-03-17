---
UID: NF:dciman.DCIBeginAccess
title: DCIBeginAccess function (dciman.h)
description: Obtains an access pointer to display frame buffer based on the given rectangle.
helpviewer_keywords: ["DCIBeginAccess","DCIBeginAccess function [Windows API]","_dciman_dcibeginaccess","dciman/DCIBeginAccess","winprog._dciman_dcibeginaccess","winui._dciman_dcibeginaccess"]
old-location: winprog\_dciman_dcibeginaccess.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dcibeginaccess.htm
ms.date: 12/05/2018
ms.keywords: DCIBeginAccess, DCIBeginAccess function [Windows API], _dciman_dcibeginaccess, dciman/DCIBeginAccess, winprog._dciman_dcibeginaccess, winui._dciman_dcibeginaccess
req.header: dciman.h
req.include-header: 
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
req.lib: Dciman32.lib
req.dll: Dciman32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCIBeginAccess
 - dciman/DCIBeginAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dciman32.dll
api_name:
 - DCIBeginAccess
---

# DCIBeginAccess function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Obtains an access pointer to display frame buffer based on the given rectangle.

## -parameters

### -param pdci [in]

A pointer to a <b>DCISURFACEINFO</b> structure.

### -param x [in]

The x-coordinate of the upper-left corner of the rectangle.

### -param y [in]

The y-coordinate of the upper-left corner of the rectangle.

### -param dx [in]

The width of the rectangle.

### -param dy [in]

The height of the rectangle.

## -returns

If the function succeeds, the return value is DCI_OK or DCI_STATUS_POINTERCHANGED.  DCI_STATUS_POINTERCHANGED indicates that the virtual address of the frame buffer could have been changed since the last call.  So the application should not assume the consistency of the virtual address of the display frame buffer.  If the function fails, the return value is one of the DCI errors.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>