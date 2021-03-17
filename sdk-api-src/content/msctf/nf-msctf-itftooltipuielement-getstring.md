---
UID: NF:msctf.ITfToolTipUIElement.GetString
title: ITfToolTipUIElement::GetString (msctf.h)
description: Returns the string of the tooltip.
helpviewer_keywords: ["GetString","GetString method [Text Services Framework]","GetString method [Text Services Framework]","ITfToolTipUIElement interface","ITfToolTipUIElement interface [Text Services Framework]","GetString method","ITfToolTipUIElement.GetString","ITfToolTipUIElement::GetString","msctf/ITfToolTipUIElement::GetString","tsf.itftooltipuielement_getstring"]
old-location: tsf\itftooltipuielement_getstring.htm
tech.root: TSF
ms.assetid: 2858a16a-7550-4e16-8872-ecfffa7d1b4e
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Text Services Framework], GetString method [Text Services Framework],ITfToolTipUIElement interface, ITfToolTipUIElement interface [Text Services Framework],GetString method, ITfToolTipUIElement.GetString, ITfToolTipUIElement::GetString, msctf/ITfToolTipUIElement::GetString, tsf.itftooltipuielement_getstring
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfToolTipUIElement::GetString
 - msctf/ITfToolTipUIElement::GetString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfToolTipUIElement.GetString
---

# ITfToolTipUIElement::GetString


## -description

Returns the string of the tooltip.

## -parameters

### -param pstr [out]

[out] A pointer to receive BSTR. This is the string for the tooltip.

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

