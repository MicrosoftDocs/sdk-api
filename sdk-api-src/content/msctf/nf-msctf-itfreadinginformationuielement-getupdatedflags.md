---
UID: NF:msctf.ITfReadingInformationUIElement.GetUpdatedFlags
title: ITfReadingInformationUIElement::GetUpdatedFlags (msctf.h)
description: This method returns the flag that tells which part of this element was updated.
helpviewer_keywords: ["GetUpdatedFlags","GetUpdatedFlags method [Text Services Framework]","GetUpdatedFlags method [Text Services Framework]","ITfReadingInformationUIElement interface","ITfReadingInformationUIElement interface [Text Services Framework]","GetUpdatedFlags method","ITfReadingInformationUIElement.GetUpdatedFlags","ITfReadingInformationUIElement::GetUpdatedFlags","TF_RIUIE_CONTEXT","TF_RIUIE_ERRORINDEX","TF_RIUIE_MAXREADINGSTRINGLENGTH","TF_RIUIE_STRING","TF_RIUIE_VERTICALORDER","msctf/ITfReadingInformationUIElement::GetUpdatedFlags","tsf.iitfreadinginformationuielement_getupdatedflags","tsf.itfreadinginformationuielement_getupdatedflags"]
old-location: tsf\itfreadinginformationuielement_getupdatedflags.htm
tech.root: TSF
ms.assetid: 6a5b1a50-9d0b-440a-a98f-80fd33c6cd95
ms.date: 12/05/2018
ms.keywords: GetUpdatedFlags, GetUpdatedFlags method [Text Services Framework], GetUpdatedFlags method [Text Services Framework],ITfReadingInformationUIElement interface, ITfReadingInformationUIElement interface [Text Services Framework],GetUpdatedFlags method, ITfReadingInformationUIElement.GetUpdatedFlags, ITfReadingInformationUIElement::GetUpdatedFlags, TF_RIUIE_CONTEXT, TF_RIUIE_ERRORINDEX, TF_RIUIE_MAXREADINGSTRINGLENGTH, TF_RIUIE_STRING, TF_RIUIE_VERTICALORDER, msctf/ITfReadingInformationUIElement::GetUpdatedFlags, tsf.iitfreadinginformationuielement_getupdatedflags, tsf.itfreadinginformationuielement_getupdatedflags
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
 - ITfReadingInformationUIElement::GetUpdatedFlags
 - msctf/ITfReadingInformationUIElement::GetUpdatedFlags
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
 - ITfReadingInformationUIElement.GetUpdatedFlags
---

# ITfReadingInformationUIElement::GetUpdatedFlags


## -description

This method returns the flag that tells which part of this element was updated.

## -parameters

### -param pdwFlags [out]

[out] A pointer to receive the flags that is a combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_CONTEXT"></a><a id="tf_riuie_context"></a><dl>
<dt><b>TF_RIUIE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The target <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_STRING"></a><a id="tf_riuie_string"></a><dl>
<dt><b>TF_RIUIE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The reading information string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_MAXREADINGSTRINGLENGTH"></a><a id="tf_riuie_maxreadingstringlength"></a><dl>
<dt><b>TF_RIUIE_MAXREADINGSTRINGLENGTH</b></dt>
</dl>
</td>
<td width="60%">
The max length of the reading information string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_ERRORINDEX"></a><a id="tf_riuie_errorindex"></a><dl>
<dt><b>TF_RIUIE_ERRORINDEX</b></dt>
</dl>
</td>
<td width="60%">
The error index of the reading information string was changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RIUIE_VERTICALORDER"></a><a id="tf_riuie_verticalorder"></a><dl>
<dt><b>TF_RIUIE_VERTICALORDER</b></dt>
</dl>
</td>
<td width="60%">
The vertical order preference was changed.

</td>
</tr>
</table>

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