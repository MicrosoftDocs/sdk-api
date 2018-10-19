---
UID: NN:msctf.IEnumITfCompositionView
title: IEnumITfCompositionView
author: windows-sdk-content
description: The IEnumITfCompositionView interface is implemented by the TSF manager to provide an enumeration of composition view objects.
old-location: tsf\ienumitfcompositionview.htm
tech.root: TSF
ms.assetid: d842b367-a605-4ed0-887d-89dfcf6893a6
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IEnumITfCompositionView, IEnumITfCompositionView interface [Text Services Framework], IEnumITfCompositionView interface [Text Services Framework],described, _tsf_ienumitfcompositionview_ref, msctf/IEnumITfCompositionView, tsf.ienumitfcompositionview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumITfCompositionView
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumITfCompositionView interface


## -description


The <b>IEnumITfCompositionView</b> interface is implemented by the TSF manager to provide an enumeration of composition view objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumITfCompositionView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumITfCompositionView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumITfCompositionView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/536b89ee-c2bd-4713-aa2c-2a2e4841a8de">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70b0dd55-41c0-4188-b79e-e49a0e203949">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0f63b58-fe9c-4c2c-8e70-e7be88030417">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9edc8dd8-4cbb-4250-a0e9-05d7250d5ad3">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

