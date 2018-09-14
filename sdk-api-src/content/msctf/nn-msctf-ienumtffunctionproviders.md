---
UID: NN:msctf.IEnumTfFunctionProviders
title: IEnumTfFunctionProviders
author: windows-sdk-content
description: The IEnumTfFunctionProviders interface is implemented by the TSF manager to provide an enumeration of function provider objects.
old-location: tsf\ienumtffunctionproviders.htm
tech.root: TSF
ms.assetid: 21e2f1c8-926e-4e53-b8d1-aecc2d1a97cb
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IEnumTfFunctionProviders, IEnumTfFunctionProviders interface [Text Services Framework], IEnumTfFunctionProviders interface [Text Services Framework],described, _tsf_ienumtffunctionproviders_ref, msctf/IEnumTfFunctionProviders, tsf.ienumtffunctionproviders
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
 - IEnumTfFunctionProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfFunctionProviders interface


## -description


The <b>IEnumTfFunctionProviders</b> interface is implemented by the TSF manager to provide an enumeration of function provider objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfFunctionProviders</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfFunctionProviders</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfFunctionProviders</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa4b8682-4f99-425d-8ae7-a510e109fe64">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9938eb0-c084-4663-9aef-584c987a08a7">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99f4b38e-bb7f-41a8-ad3a-dd0ee7213699">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb529c7c-c4fa-4dc7-a648-847ecefacf60">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

