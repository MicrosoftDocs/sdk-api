---
UID: NF:msctf.ITfReadingInformationUIElement.GetContext
title: ITfReadingInformationUIElement::GetContext (msctf.h)
description: This method returns the target ITfContext of this reading information UI.
helpviewer_keywords: ["GetContext","GetContext method [Text Services Framework]","GetContext method [Text Services Framework]","ITfReadingInformationUIElement interface","ITfReadingInformationUIElement interface [Text Services Framework]","GetContext method","ITfReadingInformationUIElement.GetContext","ITfReadingInformationUIElement::GetContext","msctf/ITfReadingInformationUIElement::GetContext","tsf.iitfreadinginformationuielement_getcontext","tsf.itfreadinginformationuielement_getcontext"]
old-location: tsf\itfreadinginformationuielement_getcontext.htm
tech.root: TSF
ms.assetid: 018c10ca-698e-42e6-9439-09f183870f91
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method [Text Services Framework], GetContext method [Text Services Framework],ITfReadingInformationUIElement interface, ITfReadingInformationUIElement interface [Text Services Framework],GetContext method, ITfReadingInformationUIElement.GetContext, ITfReadingInformationUIElement::GetContext, msctf/ITfReadingInformationUIElement::GetContext, tsf.iitfreadinginformationuielement_getcontext, tsf.itfreadinginformationuielement_getcontext
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
 - ITfReadingInformationUIElement::GetContext
 - msctf/ITfReadingInformationUIElement::GetContext
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
 - ITfReadingInformationUIElement.GetContext
---

# ITfReadingInformationUIElement::GetContext


## -description

This method returns the target <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> of this reading information UI.

## -parameters

### -param ppic [out]

[out] A pointer to receive the target <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface of this UI element.

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