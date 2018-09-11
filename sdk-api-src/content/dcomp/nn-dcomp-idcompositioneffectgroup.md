---
UID: NN:dcomp.IDCompositionEffectGroup
title: IDCompositionEffectGroup
author: windows-sdk-content
description: Represents a group of bitmap effects that are applied together to modify the rasterization of a visual's subtree.
old-location: directcomp\idcompositioneffectgroup.htm
tech.root: directcomp
ms.assetid: B8C5A4D8-F161-4383-B117-B89E85C65B19
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionEffectGroup, IDCompositionEffectGroup interface [DirectComposition], IDCompositionEffectGroup interface [DirectComposition],described, dcomp/IDCompositionEffectGroup, directcomp.idcompositioneffectgroup
ms.prod: windows
ms.technology: windows-sdk
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
 - IDCompositionEffectGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionEffectGroup interface


## -description


Represents a group of bitmap effects that are applied together to modify the rasterization of a visual's subtree.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionEffectGroup</b> interface inherits from <a href="https://msdn.microsoft.com/9C9DFECD-0EC0-446C-8CCC-BB7979B01575">IDCompositionEffect</a>. <b>IDCompositionEffectGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionEffectGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/785DE91D-718B-4704-88E4-B8FB12586E5F">SetOpacity</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Opacity property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">SetTransform3D</a>
</td>
<td align="left" width="63%">
Sets the 3D transformation effect object that modifies the rasterization of the visuals that this effect group is applied to.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9C9DFECD-0EC0-446C-8CCC-BB7979B01575">IDCompositionEffect</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

