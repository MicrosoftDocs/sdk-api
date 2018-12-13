---
UID: NN:dcomp.IDCompositionDevice
title: IDCompositionDevice
author: windows-sdk-content
description: Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
old-location: directcomp\idcompositiondevice.htm
tech.root: directcomp
ms.assetid: 081a14ed-c152-4e0a-b85b-1111d825ce53
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionDevice, IDCompositionDevice interface [DirectComposition], IDCompositionDevice interface [DirectComposition],described, dcomp/IDCompositionDevice, directcomp.idcompositiondevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IDCompositionDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice interface


## -description


Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F9916B1E-8713-4758-963A-DFD0F916FF2C">CheckDeviceState</a>
</td>
<td align="left" width="63%">
Determines whether the DirectComposition device object is still valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49a6d33d-7454-44be-b8ca-602b247d4eab">Commit</a>
</td>
<td align="left" width="63%">
Commits all DirectComposition commands that are pending on this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e32193b2-de93-417e-9fe0-49f8e45f7a01">CreateAnimation</a>
</td>
<td align="left" width="63%">
Creates an animation object that is used to animate one or more scalar properties of one or more DirectComposition objects.

  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCF3AACB-F61D-43D4-BAFB-D9453C745956">CreateEffectGroup</a>
</td>
<td align="left" width="63%">
Creates an object that represents multiple effects to be applied to a visual subtree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79291366-2fb2-4130-a642-4993648d8aa6">CreateMatrixTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D 3-by-2 matrix transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/699DB053-3897-43EC-92E2-BD45CE643130">CreateMatrixTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D 4-by-4 matrix transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b937fbf0-b920-413a-a184-ebe08ee893e5">CreateRectangleClip</a>
</td>
<td align="left" width="63%">
Creates a clip object that can be used to restrict the rendering of  a visual subtree to a rectangular area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26a58b2c-1c68-4e38-963c-4df7512347f0">CreateRotateTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D rotation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F680BDB-F845-42AD-8888-B0E4A106D9CB">CreateRotateTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D rotation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b11673dd-87c1-43c9-8501-affa1fa64c08">CreateScaleTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D scale transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B9AEEB9-559A-4B7B-A4B5-1C976B92BE7B">CreateScaleTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D scale transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c67d1c75-8704-44b3-8794-58cf08ea2572">CreateSkewTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D skew transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3B321BF8-A7A5-4E40-B548-D88CA45F6DAF">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates an updateable surface object that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/391E98B4-9FFB-4065-91A4-99306B2FEB8F">CreateSurfaceFromHandle</a>
</td>
<td align="left" width="63%">
Creates a new composition surface object that wraps an existing composition surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EA49F8EB-FAC8-421E-854D-C4AA81887EB0">CreateSurfaceFromHwnd</a>
</td>
<td align="left" width="63%">
Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eba2388a-9c94-43f0-bf7f-e814895a2792">CreateTargetForHwnd</a>
</td>
<td align="left" width="63%">
Creates a composition target object that is bound to the window that is represented by the specified window handle (<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47119ECA-CAA0-41E7-821E-18E99B6C91BD">CreateTransform3DGroup</a>
</td>
<td align="left" width="63%">
Creates a 3D transform group object that holds an array of 3D transform objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d080bd1-f8ea-4a86-89bc-f4a801917335">CreateTransformGroup</a>
</td>
<td align="left" width="63%">
Creates a 2D transform group object that holds an array of 2D transform objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15b16ff7-cf7e-455e-beb7-737f2cc21f9d">CreateTranslateTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D translation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FCB518EA-B36C-4740-9191-0BEB13AB5F06">CreateTranslateTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D translation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85619C69-F5AE-4F07-AE56-7305BBECD58F">CreateVirtualSurface</a>
</td>
<td align="left" width="63%">
Creates a sparsely populated surface that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b4fefe0-772e-42bd-8e81-37d0b128c418">CreateVisual</a>
</td>
<td align="left" width="63%">
Creates a new visual object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Retrieves information from the composition engine about composition times and the frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C921AC68-492C-4E29-876C-8857D5475B1D">WaitForCommitCompletion</a>
</td>
<td align="left" width="63%">
Waits for the composition engine to finish processing the previous call to the <a href="https://msdn.microsoft.com/49a6d33d-7454-44be-b8ca-602b247d4eab">IDCompositionDevice::Commit</a> method. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3eb5d698-3cbf-456e-aa5f-395687c68c13">DCompositionCreateDevice</a>
 

 

