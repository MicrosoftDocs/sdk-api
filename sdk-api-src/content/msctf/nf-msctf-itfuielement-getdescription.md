---
UID: NF:msctf.ITfUIElement.GetDescription
title: ITfUIElement::GetDescription (msctf.h)
author: windows-sdk-content
description: The ITfUIElement::GetDescription method returns the description of the UI element.
old-location: tsf\itfuielement_getdescription.htm
tech.root: TSF
ms.assetid: 1d6fad13-e90a-4c5a-a735-d6e54f53488f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Text Services Framework], GetDescription method [Text Services Framework],ITfUIElement interface, ITfUIElement interface [Text Services Framework],GetDescription method, ITfUIElement.GetDescription, ITfUIElement::GetDescription, msctf/ITfUIElement::GetDescription, tsf.itfuielement_getdescription
ms.topic: method
f1_keywords: ["msctf/ITfUIElement.GetDescription"]
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
 - Msctf.dll
api_name:
 - ITfUIElement.GetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfUIElement::GetDescription


## -description


The <b>ITfUIElement::GetDescription</b> method returns the description of the UI element.


## -parameters




### -param pbstrDescription [in]

[in] A pointer to BSTR that contains the description of the UI element.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



