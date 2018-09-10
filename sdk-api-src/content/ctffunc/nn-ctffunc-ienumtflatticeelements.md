---
UID: NN:ctffunc.IEnumTfLatticeElements
title: IEnumTfLatticeElements
author: windows-sdk-content
description: The IEnumTfLatticeElements interface is implemented by the TSF manager to provide an enumeration of lattice elements.
old-location: tsf\ienumtflatticeelements.htm
tech.root: TSF
ms.assetid: 5e36f052-a539-4020-8899-fb14c792c666
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumTfLatticeElements, IEnumTfLatticeElements interface [Text Services Framework], IEnumTfLatticeElements interface [Text Services Framework],described, _tsf_ienumtflatticeelements_ref, ctffunc/IEnumTfLatticeElements, tsf.ienumtflatticeelements
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sptip.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sptip.dll
api_name:
 - IEnumTfLatticeElements
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfLatticeElements interface


## -description


The <b>IEnumTfLatticeElements</b> interface is implemented by the TSF manager to provide an enumeration of lattice elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfLatticeElements</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfLatticeElements</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfLatticeElements</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/867fe614-d8c0-4987-b35a-bd5b175e6850">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/066493c9-6597-43f4-9f65-51578af00a9b">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b4b7479-33e9-4bff-8e18-f4e03060dc73">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53dbe7f0-cc1f-4ba4-9ed5-7b328c707902">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

