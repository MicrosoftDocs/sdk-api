---
UID: NN:dcomp.IDCompositionSurfaceFactory
title: IDCompositionSurfaceFactory
author: windows-sdk-content
description: Creates surface and virtual surface objects associated with an application-provided rendering device.
old-location: directcomp\idcompositionsurfacefactory.htm
tech.root: directcomp
ms.assetid: 1BB028E0-376E-42BD-82FD-08331341C93B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionSurfaceFactory, IDCompositionSurfaceFactory interface [DirectComposition], IDCompositionSurfaceFactory interface [DirectComposition],described, dcomp/IDCompositionSurfaceFactory, directcomp.idcompositionsurfacefactory
ms.topic: interface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurfaceFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSurfaceFactory interface


## -description


Creates surface and virtual surface objects associated with an application-provided rendering device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionSurfaceFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionSurfaceFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionSurfaceFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280424(v=VS.85).aspx">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates a surface object that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280425(v=VS.85).aspx">CreateVirtualSurface</a>
</td>
<td align="left" width="63%">
Creates a sparsely populated surface that can be associated with one or more visuals for composition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280354(v=VS.85).aspx">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449083(v=VS.85).aspx">IDCompositionSurface</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449133(v=VS.85).aspx">IDCompositionVirtualSurface</a>
 

 

