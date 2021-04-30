---
UID: NF:ddrawgdi.DdUnattachSurface
title: DdUnattachSurface function (ddrawgdi.h)
description: The DdUnattachSurface function removes an attachment, created with DdAttachSurface, between two kernel-mode surface objects.
helpviewer_keywords: ["DdUnattachSurface","DdUnattachSurface function [Windows API]","GdiEntry12","_dxgkernel_ddunattachsurface","ddrawgdi/DdUnattachSurface","ddrawgdi/GdiEntry12","winprog._dxgkernel_ddunattachsurface","winui._dxgkernel_ddunattachsurface"]
old-location: winprog\_dxgkernel_ddunattachsurface.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddunattachsurface.htm
ms.date: 12/05/2018
ms.keywords: DdUnattachSurface, DdUnattachSurface function [Windows API], GdiEntry12, _dxgkernel_ddunattachsurface, ddrawgdi/DdUnattachSurface, ddrawgdi/GdiEntry12, winprog._dxgkernel_ddunattachsurface, winui._dxgkernel_ddunattachsurface
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
 - DdUnattachSurface
 - ddrawgdi/DdUnattachSurface
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
 - DdUnattachSurface
 - GdiEntry12
---

# DdUnattachSurface function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

The <b>DdUnattachSurface</b> function removes an attachment, created with <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddattachsurface">DdAttachSurface</a>, between two kernel-mode surface objects.

<b>GdiEntry12</b> is defined as an alias for this function.

## -parameters

### -param pSurface [in]

Pointer to the kernel-mode surface object that was passed as the <i>pSurfaceFrom</i> parameter to <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddattachsurface">DdAttachSurface</a>.

### -param pSurfaceAttached [in]

Pointer to the kernel-mode surface object that was passed as the <i>pSurfaceTo</i> parameter to <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddattachsurface">DdAttachSurface</a>

## -remarks

It is recommended that applications use the DirectDraw 
    API which handles surface attachments in a higher-level manner.

It is not necessary to call this function since the kernel will automatically destroy all attachments when <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdidddestroysurface">DdDestroySurface</a> is called.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>