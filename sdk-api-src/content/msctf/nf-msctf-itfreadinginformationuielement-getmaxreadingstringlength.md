---
UID: NF:msctf.ITfReadingInformationUIElement.GetMaxReadingStringLength
title: ITfReadingInformationUIElement::GetMaxReadingStringLength (msctf.h)
description: The ITfReadingInformationUIElement::GetMaxReadingStringLength method returns the max string count of the reading information UI.
helpviewer_keywords: ["GetMaxReadingStringLength","GetMaxReadingStringLength method [Text Services Framework]","GetMaxReadingStringLength method [Text Services Framework]","ITfReadingInformationUIElement interface","ITfReadingInformationUIElement interface [Text Services Framework]","GetMaxReadingStringLength method","ITfReadingInformationUIElement.GetMaxReadingStringLength","ITfReadingInformationUIElement::GetMaxReadingStringLength","msctf/ITfReadingInformationUIElement::GetMaxReadingStringLength","tsf.itfreadinginformationuielement_getmaxreadingstringlength"]
old-location: tsf\itfreadinginformationuielement_getmaxreadingstringlength.htm
tech.root: TSF
ms.assetid: a26aa8d0-a447-4ebb-b892-28b959b57681
ms.date: 12/05/2018
ms.keywords: GetMaxReadingStringLength, GetMaxReadingStringLength method [Text Services Framework], GetMaxReadingStringLength method [Text Services Framework],ITfReadingInformationUIElement interface, ITfReadingInformationUIElement interface [Text Services Framework],GetMaxReadingStringLength method, ITfReadingInformationUIElement.GetMaxReadingStringLength, ITfReadingInformationUIElement::GetMaxReadingStringLength, msctf/ITfReadingInformationUIElement::GetMaxReadingStringLength, tsf.itfreadinginformationuielement_getmaxreadingstringlength
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
 - ITfReadingInformationUIElement::GetMaxReadingStringLength
 - msctf/ITfReadingInformationUIElement::GetMaxReadingStringLength
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
 - ITfReadingInformationUIElement.GetMaxReadingStringLength
---

# ITfReadingInformationUIElement::GetMaxReadingStringLength


## -description

The <b>ITfReadingInformationUIElement::GetMaxReadingStringLength</b> method returns the max string count of the reading information UI.

## -parameters

### -param pcchMax [out]

[out] A pointer to the max length of the reading information string.

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

