---
UID: NF:ddrawgdi.DdReenableDirectDrawObject
title: DdReenableDirectDrawObject function (ddrawgdi.h)
description: Wrapper for the NtGdiDdReenableDirectDrawObject function.
helpviewer_keywords: ["DdReenableDirectDrawObject","DdReenableDirectDrawObject function [Windows API]","GdiEntry10","_dxgkernel_ddreenabledirectdrawobject","ddrawgdi/DdReenableDirectDrawObject","ddrawgdi/GdiEntry10","winprog._dxgkernel_ddreenabledirectdrawobject","winui._dxgkernel_ddreenabledirectdrawobject"]
old-location: winprog\_dxgkernel_ddreenabledirectdrawobject.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddreenabledirectdrawobject.htm
ms.date: 12/05/2018
ms.keywords: DdReenableDirectDrawObject, DdReenableDirectDrawObject function [Windows API], GdiEntry10, _dxgkernel_ddreenabledirectdrawobject, ddrawgdi/DdReenableDirectDrawObject, ddrawgdi/GdiEntry10, winprog._dxgkernel_ddreenabledirectdrawobject, winui._dxgkernel_ddreenabledirectdrawobject
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
 - DdReenableDirectDrawObject
 - ddrawgdi/DdReenableDirectDrawObject
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
 - DdReenableDirectDrawObject
 - GdiEntry10
---

# DdReenableDirectDrawObject function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddreenabledirectdrawobject">NtGdiDdReenableDirectDrawObject</a> function. It re-enables a Microsoft DirectDraw driver instance after a mode switch-style event such as a true mode switch, appearance of a full-screen Microsoft MS-DOS box, or change of display driver.



<b>GdiEntry10</b> is defined as an alias for this function.

## -parameters

### -param pDirectDrawGlobal

DirectDraw object that needs to be re-enabled.

### -param pbNewMode

Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.

## -returns

If successful (the device can be re-enabled), this function returns <b>TRUE</b>. Otherwise (for example, the display driver was changed), it returns <b>FALSE</b>.

## -remarks

Once the object has been re-enabled, the capabilities for the device can be re-queried using a call to <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject">DdQueryDirectDrawObject</a> or GdiEntry2.


Applications are advised to use the 
DirectDraw or <a href="/windows/desktop/direct3d10/d3d10-graphics-reference">Direct3D</a> APIs, which automate and abstract this process in a manner independent of the operating system.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>