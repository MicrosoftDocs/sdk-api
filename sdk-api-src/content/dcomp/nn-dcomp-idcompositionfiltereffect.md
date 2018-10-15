---
UID: NN:dcomp.IDCompositionFilterEffect
title: IDCompositionFilterEffect
author: windows-sdk-content
description: Represents a filter effect.
old-location: directcomp\idcompositionfiltereffect.htm
tech.root: directcomp
ms.assetid: 4303c24d-e3e1-e188-bbef-e654c0e7e266
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionFilterEffect, IDCompositionFilterEffect interface [DirectComposition], IDCompositionFilterEffect interface [DirectComposition],described, dcomp/IDCompositionFilterEffect, directcomp.idcompositionfiltereffect
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
 - IDCompositionFilterEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionFilterEffect interface


## -description


Represents a filter effect.

IDCompositionFilterEffect exposes a subset of Direct2D's image <a href="https://msdn.microsoft.com/1446BDA9-AD4C-472C-8F1D-82ABC1880E13">effects</a> through Direction Composition for use in CSS filters in the browser platform.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionFilterEffect</b> interface inherits from <a href="https://msdn.microsoft.com/9C9DFECD-0EC0-446C-8CCC-BB7979B01575">IDCompositionEffect</a>. <b>IDCompositionFilterEffect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionFilterEffect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8DFF137E-2979-42D4-A8A5-F831A33468CA">SetInput</a>
</td>
<td align="left" width="63%">
Sets the the input at an index to the specified filter effect.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9C9DFECD-0EC0-446C-8CCC-BB7979B01575">IDCompositionEffect</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

