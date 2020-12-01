---
UID: NF:ddrawgdi.DdAttachSurface
title: DdAttachSurface function (ddrawgdi.h)
description: The DdAttachSurface function attaches two kernel-mode surface representations. GdiEntry11 is defined as an alias for this function.
helpviewer_keywords: ["DdAttachSurface","DdAttachSurface function [Windows API]","GdiEntry11","_dxgkernel_ddattachsurface","ddrawgdi/DdAttachSurface","ddrawgdi/GdiEntry11","winprog._dxgkernel_ddattachsurface","winui._dxgkernel_ddattachsurface"]
old-location: winprog\_dxgkernel_ddattachsurface.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddattachsurface.htm
ms.date: 12/05/2018
ms.keywords: DdAttachSurface, DdAttachSurface function [Windows API], GdiEntry11, _dxgkernel_ddattachsurface, ddrawgdi/DdAttachSurface, ddrawgdi/GdiEntry11, winprog._dxgkernel_ddattachsurface, winui._dxgkernel_ddattachsurface
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
 - DdAttachSurface
 - ddrawgdi/DdAttachSurface
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
 - DdAttachSurface
 - GdiEntry11
---

# DdAttachSurface function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

The <b>DdAttachSurface</b> function attaches two kernel-mode surface representations.



<b>GdiEntry11</b> is defined as an alias for this function.

## -parameters

### -param pSurfaceFrom [in]

Pointer to a kernel-mode surface object that will be the start point of the new attachment.

### -param pSurfaceTo [in]

Pointer to a kernel-mode surface object that will be the end point of the new attachment.

## -returns

<b>DdAttachSurface</b> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The function call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function call failed.

</td>
</tr>
</table>

## -remarks

See the DirectDraw 
    software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.

<div class="alert"><b>Note</b>  As with other surface attachments, the resulting attachment is one-way.  After this function is called, <i>pSurfaceTo</i> will not be attached to <i>pSurfaceFrom</i>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>