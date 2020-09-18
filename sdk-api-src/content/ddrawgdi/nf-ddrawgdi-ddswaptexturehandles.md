---
UID: NF:ddrawgdi.DdSwapTextureHandles
title: DdSwapTextureHandles function (ddrawgdi.h)
description: Developed for device driver interfaces (DDIs) prior to Microsoft DirectDraw 7.0 and does nothing on Microsoft Windows NT systems. All parameters are ignored. GdiEntry16 is defined as an alias for this function.
helpviewer_keywords: ["DdSwapTextureHandles","DdSwapTextureHandles function [Windows API]","GdiEntry16","_dxgkernel_ddswaptexturehandles","ddrawgdi/DdSwapTextureHandles","ddrawgdi/GdiEntry16","winprog._dxgkernel_ddswaptexturehandles","winui._dxgkernel_ddswaptexturehandles"]
old-location: winprog\_dxgkernel_ddswaptexturehandles.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddswaptexturehandles.htm
ms.date: 12/05/2018
ms.keywords: DdSwapTextureHandles, DdSwapTextureHandles function [Windows API], GdiEntry16, _dxgkernel_ddswaptexturehandles, ddrawgdi/DdSwapTextureHandles, ddrawgdi/GdiEntry16, winprog._dxgkernel_ddswaptexturehandles, winui._dxgkernel_ddswaptexturehandles
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
 - DdSwapTextureHandles
 - ddrawgdi/DdSwapTextureHandles
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
 - DdSwapTextureHandles
 - GdiEntry16
---

# DdSwapTextureHandles function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Developed for device driver interfaces (DDIs) prior to Microsoft DirectDraw 7.0 and does nothing on Microsoft Windows NT systems. All parameters are ignored.


<b>GdiEntry16</b> is defined as an alias for this function.

## -parameters

### -param pDDraw

Reserved.

### -param pDDSLcl1

Reserved.

### -param pDDSLcl2

Reserved.

## -returns

DDHAL_DRIVER_HANDLED is returned.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>