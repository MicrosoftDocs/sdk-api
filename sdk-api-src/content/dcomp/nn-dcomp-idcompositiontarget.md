---
UID: NN:dcomp.IDCompositionTarget
title: IDCompositionTarget
author: windows-sdk-content
description: Represents a binding between a Microsoft DirectComposition visual tree and a destination on top of which the visual tree should be composed.
old-location: directcomp\idcompositiontarget.htm
tech.root: directcomp
ms.assetid: 86dbfe68-e360-42cf-b572-960398ef06ba
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionTarget, IDCompositionTarget interface [DirectComposition], IDCompositionTarget interface [DirectComposition],described, dcomp/IDCompositionTarget, directcomp.idcompositiontarget
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
 - IDCompositionTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionTarget interface


## -description


Represents a binding between a Microsoft DirectComposition visual tree and a destination on top of which the visual tree should be composed. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/febbef70-fc21-4295-93c5-2f9f52434aae">SetRoot</a>
</td>
<td align="left" width="63%">
Sets a visual object as the new root object of a visual tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/eba2388a-9c94-43f0-bf7f-e814895a2792">IDCompositionDevice::CreateTargetForHwnd</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

