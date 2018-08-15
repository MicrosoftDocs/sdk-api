---
UID: NF:dcomp.SetClip
title: SetClip function
author: windows-sdk-content
description: Sets the Clip property of this visual to the specified rectangular region or clip object.
old-location: directcomp\idcompositionvisual_setclip_overloaded.htm
old-project: directcomp
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionVisual::SetClip, SetClip, SetClip methods [DirectComposition], dcomp/SetClip, directcomp.idcompositionvisual_setclip_overloaded
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual::SetClip
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# SetClip function


## -description


<span>Sets the Clip property of this visual to the specified rectangular region or clip object. The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7F01EB25-3A44-416F-A926-D185F2FD44EC">SetClip(const D2D_RECT_F&)</a>
</td>
<td align="left" width="63%">
Sets the Clip property to the specified rectangular region.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/504938a1-2775-477d-a077-7afc4e333f36">SetClip(IDCompositionClip*)</a>
</td>
<td align="left" width="63%">
Sets the Clip property to the specified clip object.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/B6E0D8F5-B6B9-40CC-B079-850AC8F2D538">Clipping</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

