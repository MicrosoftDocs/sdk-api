---
UID: NF:ddrawgdi.DdDeleteDirectDrawObject
title: DdDeleteDirectDrawObject function (ddrawgdi.h)
description: Wrapper for the NtGdiDdDeleteDirectDrawObject function and deletes a kernel-mode Microsoft DirectDraw object that was previously created using DdCreateDirectDrawObject. GdiEntry3 is defined as an alias for this function.
helpviewer_keywords: ["DdDeleteDirectDrawObject","DdDeleteDirectDrawObject function [Windows API]","GdiEntry3","_dxgkernel_dddeletedirectdrawobject","ddrawgdi/DdDeleteDirectDrawObject","ddrawgdi/GdiEntry3","winprog._dxgkernel_dddeletedirectdrawobject","winui._dxgkernel_dddeletedirectdrawobject"]
old-location: winprog\_dxgkernel_dddeletedirectdrawobject.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dddeletedirectdrawobject.htm
ms.date: 12/05/2018
ms.keywords: DdDeleteDirectDrawObject, DdDeleteDirectDrawObject function [Windows API], GdiEntry3, _dxgkernel_dddeletedirectdrawobject, ddrawgdi/DdDeleteDirectDrawObject, ddrawgdi/GdiEntry3, winprog._dxgkernel_dddeletedirectdrawobject, winui._dxgkernel_dddeletedirectdrawobject
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
 - DdDeleteDirectDrawObject
 - ddrawgdi/DdDeleteDirectDrawObject
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
 - DdDeleteDirectDrawObject
 - GdiEntry3
---

# DdDeleteDirectDrawObject function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdidddeletedirectdrawobject">NtGdiDdDeleteDirectDrawObject</a> function and deletes a kernel-mode Microsoft DirectDraw object that was previously created using <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject">DdCreateDirectDrawObject</a>.


<b>GdiEntry3</b> is defined as an alias for this function.

## -parameters

### -param pDirectDrawGlobal

Pointer to the user-mode DirectDraw object. See the DDK documentation for details.

## -returns

If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

Applications are advised to use the 
DirectDraw and 
<a href="/windows/desktop/direct3d10/d3d10-graphics-reference">Direct3D</a> APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>