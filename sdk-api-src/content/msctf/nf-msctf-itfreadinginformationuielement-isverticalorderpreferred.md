---
UID: NF:msctf.ITfReadingInformationUIElement.IsVerticalOrderPreferred
title: ITfReadingInformationUIElement::IsVerticalOrderPreferred (msctf.h)
description: This method returns if the UI prefers to be shown in vertical order.
helpviewer_keywords: ["ITfReadingInformationUIElement interface [Text Services Framework]","IsVerticalOrderPreferred method","ITfReadingInformationUIElement.IsVerticalOrderPreferred","ITfReadingInformationUIElement::IsVerticalOrderPreferred","IsVerticalOrderPreferred","IsVerticalOrderPreferred method [Text Services Framework]","IsVerticalOrderPreferred method [Text Services Framework]","ITfReadingInformationUIElement interface","msctf/ITfReadingInformationUIElement::IsVerticalOrderPreferred","tsf.iitfreadinginformationuielement_isverticalorderpreferred","tsf.itfreadinginformationuielement_isverticalorderpreferred"]
old-location: tsf\itfreadinginformationuielement_isverticalorderpreferred.htm
tech.root: TSF
ms.assetid: a45d8928-5cfd-4af9-ba3b-7171e48d81c8
ms.date: 12/05/2018
ms.keywords: ITfReadingInformationUIElement interface [Text Services Framework],IsVerticalOrderPreferred method, ITfReadingInformationUIElement.IsVerticalOrderPreferred, ITfReadingInformationUIElement::IsVerticalOrderPreferred, IsVerticalOrderPreferred, IsVerticalOrderPreferred method [Text Services Framework], IsVerticalOrderPreferred method [Text Services Framework],ITfReadingInformationUIElement interface, msctf/ITfReadingInformationUIElement::IsVerticalOrderPreferred, tsf.iitfreadinginformationuielement_isverticalorderpreferred, tsf.itfreadinginformationuielement_isverticalorderpreferred
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
 - ITfReadingInformationUIElement::IsVerticalOrderPreferred
 - msctf/ITfReadingInformationUIElement::IsVerticalOrderPreferred
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
 - ITfReadingInformationUIElement.IsVerticalOrderPreferred
---

# ITfReadingInformationUIElement::IsVerticalOrderPreferred


## -description

This method returns if the UI prefers to be shown in vertical order.

## -parameters

### -param pfVertical [out]

[out] True if the UI prefers to be shown in the vertical order.

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

