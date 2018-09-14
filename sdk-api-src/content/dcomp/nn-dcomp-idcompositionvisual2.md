---
UID: NN:dcomp.IDCompositionVisual2
title: IDCompositionVisual2
author: windows-sdk-content
description: Represents one DirectComposition visual in a visual tree.
old-location: directcomp\idcompositionvisual2.htm
tech.root: directcomp
ms.assetid: D4D04A43-BF00-482A-9CDD-A476BD1CB953
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDCompositionVisual2, IDCompositionVisual2 interface [DirectComposition], IDCompositionVisual2 interface [DirectComposition],described, dcomp/IDCompositionVisual2, directcomp.idcompositionvisual2
ms.prod: windows
ms.technology: windows-sdk
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
 - IDCompositionVisual2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual2 interface


## -description


Represents one DirectComposition visual in a visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionVisual2</b> interface inherits from <a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>. <b>IDCompositionVisual2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionVisual2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A488A0B9-3CBE-477A-9688-84A7DA43D7F6">SetBackFaceVisibility</a>
</td>
<td align="left" width="63%">
Specifies whether or not surfaces that have 3D transformations applied to them should be displayed when facing away from the observer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8802266E-9D31-409E-ACE8-62A3E9E93EA3">SetOpacityMode</a>
</td>
<td align="left" width="63%">
Sets the opacity mode for this visual.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=313910">DirectComposition Backface and D2D Batching</a>



<a href="https://msdn.microsoft.com/CCF66B7A-5847-425C-92A4-969C8B915132">IDCompositionDevice2::CreateVisual</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>



<b>Sample</b>
 

 

