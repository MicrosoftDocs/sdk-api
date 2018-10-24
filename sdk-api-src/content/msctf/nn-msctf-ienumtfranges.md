---
UID: NN:msctf.IEnumTfRanges
title: IEnumTfRanges
author: windows-sdk-content
description: The IEnumTfRanges interface is implemented by the TSF manager to provide an enumeration of range objects.
old-location: tsf\ienumtfranges.htm
tech.root: TSF
ms.assetid: 68e17539-3b00-4e51-964d-0516b448f6c8
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnumTfRanges, IEnumTfRanges interface [Text Services Framework], IEnumTfRanges interface [Text Services Framework],described, _tsf_ienumtfranges_ref, msctf/IEnumTfRanges, tsf.ienumtfranges
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
 - IEnumTfRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfRanges interface


## -description


The <b>IEnumTfRanges</b> interface is implemented by the TSF manager to provide an enumeration of range objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfRanges</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfRanges</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfRanges</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e51a747-0b77-4ba3-b03c-217a3f81a0aa">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95fe45f0-bf30-4f8c-86f3-e20a0d70127e">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7f8ea8d-5627-4dc1-ab22-a9e14f536520">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f13ec6c2-379f-42e1-af92-62c4a8d8d922">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

