---
UID: NN:msctf.IEnumTfDisplayAttributeInfo
title: IEnumTfDisplayAttributeInfo
author: windows-sdk-content
description: The IEnumTfDisplayAttributeInfo interface is implemented by the TSF manager to provide an enumeration of display attribute information objects.
old-location: tsf\ienumtfdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: b222deb8-22dd-44c3-9ecc-0fb379682796
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IEnumTfDisplayAttributeInfo, IEnumTfDisplayAttributeInfo interface [Text Services Framework], IEnumTfDisplayAttributeInfo interface [Text Services Framework],described, _tsf_ienumtfdisplayattributeinfo_ref, msctf/IEnumTfDisplayAttributeInfo, tsf.ienumtfdisplayattributeinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEnumTfDisplayAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfDisplayAttributeInfo interface


## -description


The <b>IEnumTfDisplayAttributeInfo</b> interface is implemented by the TSF manager to provide an enumeration of display attribute information objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfDisplayAttributeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfDisplayAttributeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfDisplayAttributeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cf57360-b07b-4a6c-850a-10c44895108d">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db374ba3-8a65-4933-85cb-320c294d6041">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdfcf505-ae4a-4f7e-91f2-3e79efd56162">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c4c9ca9-a813-406f-a507-16ccb0ff2a2a">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

