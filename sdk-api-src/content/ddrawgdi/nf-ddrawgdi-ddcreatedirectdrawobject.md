---
UID: NF:ddrawgdi.DdCreateDirectDrawObject
title: DdCreateDirectDrawObject function (ddrawgdi.h)
description: Wrapper for the NtGdiDdCreateDirectDrawObject function and creates a kernel-side representation of the Microsoft DirectDraw object.
helpviewer_keywords: ["DdCreateDirectDrawObject","DdCreateDirectDrawObject function [Windows API]","GdiEntry1","_dxgkernel_ddcreatedirectdrawobject","ddrawgdi/DdCreateDirectDrawObject","ddrawgdi/GdiEntry1","winprog._dxgkernel_ddcreatedirectdrawobject","winui._dxgkernel_ddcreatedirectdrawobject"]
old-location: winprog\_dxgkernel_ddcreatedirectdrawobject.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddcreatedirectdrawobject.htm
ms.date: 12/05/2018
ms.keywords: DdCreateDirectDrawObject, DdCreateDirectDrawObject function [Windows API], GdiEntry1, _dxgkernel_ddcreatedirectdrawobject, ddrawgdi/DdCreateDirectDrawObject, ddrawgdi/GdiEntry1, winprog._dxgkernel_ddcreatedirectdrawobject, winui._dxgkernel_ddcreatedirectdrawobject
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
 - DdCreateDirectDrawObject
 - ddrawgdi/DdCreateDirectDrawObject
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
 - DdCreateDirectDrawObject
 - GdiEntry1
---

# DdCreateDirectDrawObject function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddcreatedirectdrawobject">NtGdiDdCreateDirectDrawObject</a> function and creates a kernel-side representation of the Microsoft DirectDraw object. A handle to this representation will be stored in <i>pDirectDrawGlobal</i>-&gt;hDD.


<b>GdiEntry1</b> is defined as an alias for this function.

## -parameters

### -param pDirectDrawGlobal

Pointer to the user-mode DirectDraw object. See DDK documentation for details.

### -param hdc

Handle to the DC for the device for which this representation is created. If 0, device will be the "display" device. Note that this function retains only one "display" DirectDraw object, and it will return a copied handle to that same object if subsequently called with <i>hdc</i> = 0.

## -returns

If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

Applications are advised to use the 
DirectDraw and 
<a href="/windows/desktop/direct3d10/d3d10-graphics-reference">Direct3D</a> APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>