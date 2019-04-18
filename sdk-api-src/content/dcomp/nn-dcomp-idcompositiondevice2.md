---
UID: NN:dcomp.IDCompositionDevice2
title: IDCompositionDevice2 (dcomp.h)
author: windows-sdk-content
description: Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
old-location: directcomp\idcompositiondevice2.htm
tech.root: directcomp
ms.assetid: 0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/8C24DE03-CF1E-4DC4-8C27-913DAD278579">Commit</a>
</td>
<td align="left" width="63%">
Commits all DirectComposition commands that are pending on this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F15F6CD-E2EE-42E5-AF46-01A9A28F4896">CreateAnimation</a>
</td>
<td align="left" width="63%">
Creates an animation object that is used to animate one or more scalar properties of one or more DirectComposition objects.

  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07AF43F9-1050-48C5-B37B-787B5CC60E9D">CreateEffectGroup</a>
</td>
<td align="left" width="63%">
Creates an object that represents multiple effects to be applied to a visual subtree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E8D8560-F7D3-4075-A4E9-00AFCEB526BE">CreateMatrixTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D 3-by-2 matrix transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD187D78-7F53-45E7-AF8C-BEB7F28AFF2A">CreateMatrixTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D 4-by-4 matrix transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5CD7BC88-EF6F-4FEE-940B-710CB56D8E78">CreateRectangleClip</a>
</td>
<td align="left" width="63%">
Creates a clip object that can be used to restrict the rendering of  a visual subtree to a rectangular area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4F0187C-FB3C-447A-AD1E-5094004273F5">CreateRotateTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D rotation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F665A6EB-2EF2-4B65-BD89-84F78B5AD468">CreateRotateTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D rotation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/800BA1EF-C801-4E93-BBA0-6C8FD0ACCB68">CreateScaleTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D scale transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33B2C0D6-52D6-4443-9F30-A86C0F7BA627">CreateScaleTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D scale transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10700E97-C799-4FC0-8300-B5347CC67AC3">CreateSkewTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D skew transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1CBE92B6-AC48-47F1-B50A-B78030D356D8">CreateSurface</a>
</td>
<td align="left" width="63%">
Creates an updateable surface object that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20E60EAE-68CB-45B8-BC50-3D12F449AA6E">CreateSurfaceFactory</a>
</td>
<td align="left" width="63%">
Creates a DirectComposition surface factory object, which can be used to create other DirectComposition surface or virtual surface objects

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0B7049D1-CCAD-44EE-B398-20E763D956C2">CreateTransform3DGroup</a>
</td>
<td align="left" width="63%">
Creates a 3D transform group object that holds an array of 3D transform objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D71C813E-1660-4BA6-961D-A0EB77D16FC2">CreateTransformGroup</a>
</td>
<td align="left" width="63%">
Creates a 2D transform group object that holds an array of 2D transform objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83800B10-7992-4A3D-B8D6-6872BAEAF7DA">CreateTranslateTransform</a>
</td>
<td align="left" width="63%">
Creates a 2D translation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7913D11B-5563-4921-B455-C34069AC7BCD">CreateTranslateTransform3D</a>
</td>
<td align="left" width="63%">
Creates a 3D translation transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/659D79E3-2E7C-4431-B724-7AC2978BD9BC">CreateVirtualSurface</a>
</td>
<td align="left" width="63%">
Creates a sparsely populated surface that can be associated with one or more visuals for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CCF66B7A-5847-425C-92A4-969C8B915132">CreateVisual</a>
</td>
<td align="left" width="63%">
Creates a new visual object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C529575-46AC-495A-9165-15FC8F6B1F69">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Retrieves information from the composition engine about composition times and the frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98C790BD-5C51-4A77-9DB4-51A263A4EC2A">WaitForCommitCompletion</a>
</td>
<td align="left" width="63%">
Waits for the composition engine to finish processing the previous call to the <a href="https://msdn.microsoft.com/8C24DE03-CF1E-4DC4-8C27-913DAD278579">IDCompositionDevice2::Commit</a> method. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/C40694CB-7110-4ED0-B2E5-F73ADEA7BEA4">DCompositionCreateDevice2</a>
 

 

