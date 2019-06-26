---
UID: NN:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop
title: ICompositionDrawingSurfaceInterop (windows.ui.composition.interop.h)
author: windows-sdk-content
description: Native interoperation interface that allows drawing on a surface object using a RECT to define the area to draw into. This interface is available in C++ only.
old-location: w_ui_comp\icompositiondrawingsurfaceinterop.htm
tech.root: w_ui_comp
ms.assetid: C8A94128-009A-4327-8E77-A4E155D0910E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICompositionDrawingSurfaceInterop, ICompositionDrawingSurfaceInterop interface, ICompositionDrawingSurfaceInterop interface,described, w_ui_comp.icompositiondrawingsurfaceinterop, windows/ICompositionDrawingSurfaceInterop
ms.topic: interface
f1_keywords: 
 - "windows.ui.composition.interop/ICompositionDrawingSurfaceInterop"
req.header: windows.ui.composition.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositionDrawingSurfaceInterop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICompositionDrawingSurfaceInterop interface


## -description


Native interoperation interface that allows drawing on a surface object using a RECT to define the area to draw into.
          This interface is available in C++ only.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICompositionDrawingSurfaceInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICompositionDrawingSurfaceInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICompositionDrawingSurfaceInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-begindraw">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates drawing on the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-enddraw">EndDraw</a>
</td>
<td align="left" width="63%">
Marks the end of drawing on the surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-resize">Resize</a>
</td>
<td align="left" width="63%">
Changes the size of the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-resumedraw">ResumeDraw</a>
</td>
<td align="left" width="63%">
Resumes drawing on the surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-scroll">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls a rectangular area of the logical surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-suspenddraw">SuspendDraw</a>
</td>
<td align="left" width="63%">
Suspends drawing on the surface object.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=692061">Composition Native Interoperation Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

