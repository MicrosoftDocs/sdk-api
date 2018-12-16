---
UID: NN:dcomp.IDCompositionDevice2
title: IDCompositionDevice2
author: windows-sdk-content
description: Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
old-location: directcomp\idcompositiondevice2.htm
tech.root: directcomp
ms.assetid: 0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionDevice2, IDCompositionDevice2 interface [DirectComposition], IDCompositionDevice2 interface [DirectComposition],described, dcomp/IDCompositionDevice2, directcomp.idcompositiondevice2
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
 - IDCompositionDevice2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2 interface


## -description


Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDevice2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionDevice2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionDevice2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280355(v=VS.85).aspx">Commit</a>
</td>
<td align="left" width="63%">
Commits all DirectComposition commands that are pending on this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280356(v=VS.85).aspx">CreateAnimation</a>
</td>
<td align="left" width="63%">
Creates an animation object that is used to animate one or more scalar properties of one or more DirectComposition objects.

  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280357(v=VS.85).aspx">CreateEffectGroup</a>
</td>
<td align="left" width="63%">
Creates an object that represents multiple effects to be applied to a visual subtree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280358(v=VS.85).aspx">CreateMatrixTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D 3-by-2 matrix transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280359(v=VS.85).aspx">CreateMatrixTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D 4-by-4 matrix transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280360(v=VS.85).aspx">CreateRectangleClip</a>
</td>
<td align="left" width="63%">
Creates a clip object that can be used to restrict the rendering of  a visual subtree to a rectangular area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280361(v=VS.85).aspx">CreateRotateTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D rotation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280362(v=VS.85).aspx">CreateRotateTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D rotation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280363(v=VS.85).aspx">CreateScaleTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D scale transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280364(v=VS.85).aspx">CreateScaleTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D scale transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280365(v=VS.85).aspx">CreateSkewTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D skew transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280366(v=VS.85).aspx">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates an updateable surface object that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280367(v=VS.85).aspx">CreateSurfaceFactory</a>
</td>
<td align="left" width="63%">
Creates a DirectComposition surface factory object, which can be used to create other DirectComposition surface or virtual surface objects

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280368(v=VS.85).aspx">CreateTransform3DGroup</a>
</td>
<td align="left" width="63%">
Creates a 3D transform group object that holds an array of 3D transform objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280369(v=VS.85).aspx">CreateTransformGroup</a>
</td>
<td align="left" width="63%">
Creates a 2D transform group object that holds an array of 2D transform objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280370(v=VS.85).aspx">CreateTranslateTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D translation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280371(v=VS.85).aspx">CreateTranslateTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D translation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280372(v=VS.85).aspx">CreateVirtualSurface</a>
</td>
<td align="left" width="63%">
Creates a sparsely populated surface that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280373(v=VS.85).aspx">CreateVisual</a>
</td>
<td align="left" width="63%">
Creates a new visual object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280375(v=VS.85).aspx">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Retrieves information from the composition engine about composition times and the frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280376(v=VS.85).aspx">WaitForCommitCompletion</a>
</td>
<td align="left" width="63%">
Waits for the composition engine to finish processing the previous call to the <a href="https://msdn.microsoft.com/en-us/library/Dn280355(v=VS.85).aspx">IDCompositionDevice2::Commit</a> method. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280347(v=VS.85).aspx">DCompositionCreateDevice2</a>
 

 

