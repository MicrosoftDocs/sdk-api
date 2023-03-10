---
UID: NF:msctf.ITfReadingInformationUIElement.GetErrorIndex
title: ITfReadingInformationUIElement::GetErrorIndex (msctf.h)
description: This method returns the char index where the typing error occurs.
helpviewer_keywords: ["GetErrorIndex","GetErrorIndex method [Text Services Framework]","GetErrorIndex method [Text Services Framework]","ITfReadingInformationUIElement interface","ITfReadingInformationUIElement interface [Text Services Framework]","GetErrorIndex method","ITfReadingInformationUIElement.GetErrorIndex","ITfReadingInformationUIElement::GetErrorIndex","msctf/ITfReadingInformationUIElement::GetErrorIndex","tsf.iitfreadinginformationuielement_geterrorindex","tsf.itfreadinginformationuielement_geterrorindex"]
old-location: tsf\itfreadinginformationuielement_geterrorindex.htm
tech.root: TSF
ms.assetid: c31bfbe7-c31a-485a-a122-14215d661ce7
ms.date: 12/05/2018
ms.keywords: GetErrorIndex, GetErrorIndex method [Text Services Framework], GetErrorIndex method [Text Services Framework],ITfReadingInformationUIElement interface, ITfReadingInformationUIElement interface [Text Services Framework],GetErrorIndex method, ITfReadingInformationUIElement.GetErrorIndex, ITfReadingInformationUIElement::GetErrorIndex, msctf/ITfReadingInformationUIElement::GetErrorIndex, tsf.iitfreadinginformationuielement_geterrorindex, tsf.itfreadinginformationuielement_geterrorindex
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfReadingInformationUIElement::GetErrorIndex
 - msctf/ITfReadingInformationUIElement::GetErrorIndex
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
 - ITfReadingInformationUIElement.GetErrorIndex
---

# ITfReadingInformationUIElement::GetErrorIndex


## -description

This method returns the char index where the typing error occurs.

## -parameters

### -param pErrorIndex [out]

[out] A pointer to receive the char index where the typing error occurs.

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

