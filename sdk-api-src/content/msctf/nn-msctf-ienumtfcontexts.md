---
UID: NN:msctf.IEnumTfContexts
title: IEnumTfContexts
author: windows-sdk-content
description: The IEnumTfContexts interface is implemented by the TSF manager to provide an enumeration of context objects.
old-location: tsf\ienumtfcontexts.htm
tech.root: TSF
ms.assetid: 20b342e6-cac4-4bc5-820b-e397e0ce4648
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnumTfContexts, IEnumTfContexts interface [Text Services Framework], IEnumTfContexts interface [Text Services Framework],described, _tsf_ienumtfcontexts_ref, msctf/IEnumTfContexts, tsf.ienumtfcontexts
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
 - IEnumTfContexts
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfContexts interface


## -description


The <b>IEnumTfContexts</b> interface is implemented by the TSF manager to provide an enumeration of context objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfContexts</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfContexts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfContexts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e9486b7-5251-41b9-b36c-36a0d6dfaf5d">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0727ae8b-a66f-42a7-bc74-4c01bfff3855">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfe1d8a3-5a5f-4397-b972-ee42358aeb66">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68f0c073-0ba5-4a46-a459-b213145aebd6">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

