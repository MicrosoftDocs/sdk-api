---
UID: NF:ddrawgdi.DdDeleteSurfaceObject
title: DdDeleteSurfaceObject function (ddrawgdi.h)
description: Wrapper for the NtGdiDdDeleteSurfaceObject function and deletes a kernel-mode surface object previously created by NtGdiDdCreateSurfaceObject. GdiEntry5 is defined as an alias for this function.
helpviewer_keywords: ["DdDeleteSurfaceObject","DdDeleteSurfaceObject function [Windows API]","GdiEntry5","_dxgkernel_dddeletesurfaceobject","ddrawgdi/DdDeleteSurfaceObject","ddrawgdi/GdiEntry5","winprog._dxgkernel_dddeletesurfaceobject","winui._dxgkernel_dddeletesurfaceobject"]
old-location: winprog\_dxgkernel_dddeletesurfaceobject.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dddeletesurfaceobject.htm
ms.date: 12/05/2018
ms.keywords: DdDeleteSurfaceObject, DdDeleteSurfaceObject function [Windows API], GdiEntry5, _dxgkernel_dddeletesurfaceobject, ddrawgdi/DdDeleteSurfaceObject, ddrawgdi/GdiEntry5, winprog._dxgkernel_dddeletesurfaceobject, winui._dxgkernel_dddeletesurfaceobject
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
 - DdDeleteSurfaceObject
 - ddrawgdi/DdDeleteSurfaceObject
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
 - DdDeleteSurfaceObject
 - GdiEntry5
---

# DdDeleteSurfaceObject function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdidddeletesurfaceobject">NtGdiDdDeleteSurfaceObject</a> function and deletes a kernel-mode surface object previously created by <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddcreatesurfaceobject">NtGdiDdCreateSurfaceObject</a>.


<b>GdiEntry5</b> is defined as an alias for this function.

## -parameters

### -param pSurfaceLocal

Pointer to the user-mode surface object that has a valid <b>hDDSurface</b>. See the DDK documentation for details.

## -returns

If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

Applications are advised to use the 
DirectDraw and 
<a href="/windows/desktop/direct3d10/d3d10-graphics-reference">Direct3D</a> APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.

## -see-also

<a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject">DdCreateSurfaceObject</a>



<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>