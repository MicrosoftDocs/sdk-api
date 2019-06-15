---
UID: NN:msctf.IEnumTfPropertyValue
title: IEnumTfPropertyValue (msctf.h)
author: windows-sdk-content
description: The IEnumTfPropertyValue interface is implemented by the TSF manager to provide an enumeration of property values.
old-location: tsf\ienumtfpropertyvalue.htm
tech.root: TSF
ms.assetid: 7f99df15-777c-46eb-bff3-542eb1fcc428
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumTfPropertyValue, IEnumTfPropertyValue interface [Text Services Framework], IEnumTfPropertyValue interface [Text Services Framework],described, _tsf_ienumtfpropertyvalue_ref, msctf/IEnumTfPropertyValue, tsf.ienumtfpropertyvalue
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
 - IEnumTfPropertyValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfPropertyValue interface


## -description


The <b>IEnumTfPropertyValue</b> interface is implemented by the TSF manager to provide an enumeration of property values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfPropertyValue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTfPropertyValue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfPropertyValue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfpropertyvalue-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfpropertyvalue-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfpropertyvalue-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-ienumtfpropertyvalue-skip">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

