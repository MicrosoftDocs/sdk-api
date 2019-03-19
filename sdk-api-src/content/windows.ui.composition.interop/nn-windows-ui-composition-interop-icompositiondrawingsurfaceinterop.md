---
UID: NN:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop
title: ICompositionDrawingSurfaceInterop (windows.ui.composition.interop.h)
author: windows-sdk-content
description: Native interoperation interface that allows drawing on a surface object using a RECT to define the area to draw into. This interface is available in C++ only.
old-location: w_ui_comp\icompositiondrawingsurfaceinterop.htm
tech.root: w_ui_comp
ms.assetid: C8A94128-009A-4327-8E77-A4E155D0910E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICompositionDrawingSurfaceInterop, ICompositionDrawingSurfaceInterop interface, ICompositionDrawingSurfaceInterop interface,described, w_ui_comp.icompositiondrawingsurfaceinterop, windows/ICompositionDrawingSurfaceInterop
ms.topic: interface
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
---

# ICompositionDrawingSurfaceInterop interface


## -description


Native interoperation interface that allows drawing on a surface object using a RECT to define the area to draw into.
          This interface is available in C++ only.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICompositionDrawingSurfaceInterop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICompositionDrawingSurfaceInterop</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/01273B2A-0305-4F1E-8461-7956EDD651A7">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates drawing on the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8592A6E-8D54-49DE-B520-51F947BDDFAD">EndDraw</a>
</td>
<td align="left" width="63%">
Marks the end of drawing on the surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DFD0812F-3AD2-4E33-BD23-9D392BFAB467">Resize</a>
</td>
<td align="left" width="63%">
Changes the size of the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/083B2EDB-2C0D-4AEB-B955-A73C47960B09">ResumeDraw</a>
</td>
<td align="left" width="63%">
Resumes drawing on the surface object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0FC12E3E-B104-4E61-817A-3F56C8DAC755">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls a rectangular area of the logical surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F8FEA76A-C271-44D6-9314-88E4AE535953">SuspendDraw</a>
</td>
<td align="left" width="63%">
Suspends drawing on the surface object.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=692061">Composition Native Interoperation Overview</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

