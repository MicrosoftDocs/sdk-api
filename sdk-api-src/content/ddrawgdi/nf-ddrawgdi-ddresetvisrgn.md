---
UID: NF:ddrawgdi.DdResetVisrgn
title: DdResetVisrgn function (ddrawgdi.h)
description: Wrapper for the NtGdiDdResetVisrgn function and enables timely user-mode information on the clipping region for windows on the desktop.
helpviewer_keywords: ["DdResetVisrgn","DdResetVisrgn function [Windows API]","GdiEntry6","_dxgkernel_ddresetvisrgn","ddrawgdi/DdResetVisrgn","ddrawgdi/GdiEntry6","winprog._dxgkernel_ddresetvisrgn","winui._dxgkernel_ddresetvisrgn"]
old-location: winprog\_dxgkernel_ddresetvisrgn.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddresetvisrgn.htm
ms.date: 12/05/2018
ms.keywords: DdResetVisrgn, DdResetVisrgn function [Windows API], GdiEntry6, _dxgkernel_ddresetvisrgn, ddrawgdi/DdResetVisrgn, ddrawgdi/GdiEntry6, winprog._dxgkernel_ddresetvisrgn, winui._dxgkernel_ddresetvisrgn
req.header: ddrawgdi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdResetVisrgn
 - ddrawgdi/DdResetVisrgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddrawgdi.h
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - DdResetVisrgn
 - GdiEntry6
---

# DdResetVisrgn function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddresetvisrgn">NtGdiDdResetVisrgn</a> function and enables timely user-mode information on the clipping region for windows on the desktop.

<b>GdiEntry6</b> is defined as an alias for this function.

## -parameters

### -param pSurfaceLocal

Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset. See the DDK documentation for details.

### -param hWnd

Reserved.

## -returns

If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

Clipping can change asynchronously from the point of view of user-mode threads. 
The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes. A call to this function records this counter with every existing DirectDraw primary surface on the system.

At any later time when one of these primary surfaces is modified by a <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a> or <a href="/previous-versions/ms858221(v=msdn.10)">IDirectDrawSurface7::Lock</a> operation (see DDK documentation), the counter recorded with the surface is compared with the global counter. If these values are different, an error code DDERR_VISRGNCHANGED is returned to the user-mode code. The user-mode code will then re-query the current clipping for the desktop, call <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddresetvisrgn">NtGdiDdResetVisrgn</a>, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping. Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.

Applications are advised to use the <a href="/previous-versions/aa919448(v=msdn.10)">IDirectDrawClipper</a> interface or <a href="/previous-versions/ms889707(v=msdn.10)">IDirect3DDevice8::Present</a> method to handle asynchronous clipping changes. These constructs implement asynchronous clipping in an automated and operating-system-independent way.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>