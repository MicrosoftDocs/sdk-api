---
UID: NF:msctf.ITfReverseConversionList.GetString
title: ITfReverseConversionList::GetString (msctf.h)
description: Retrieves the keystroke sequence at the specified index.
helpviewer_keywords: ["GetString","GetString method [Text Services Framework]","GetString method [Text Services Framework]","ITfReverseConversionList interface","ITfReverseConversionList interface [Text Services Framework]","GetString method","ITfReverseConversionList.GetString","ITfReverseConversionList::GetString","msctf/ITfReverseConversionList::GetString","tsf.itfreverseconversionlist_getstring"]
old-location: tsf\itfreverseconversionlist_getstring.htm
tech.root: TSF
ms.assetid: 5a8cc79f-d348-4fe8-b005-aeabd6db43c5
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Text Services Framework], GetString method [Text Services Framework],ITfReverseConversionList interface, ITfReverseConversionList interface [Text Services Framework],GetString method, ITfReverseConversionList.GetString, ITfReverseConversionList::GetString, msctf/ITfReverseConversionList::GetString, tsf.itfreverseconversionlist_getstring
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfReverseConversionList::GetString
 - msctf/ITfReverseConversionList::GetString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfReverseConversionList.GetString
---

# ITfReverseConversionList::GetString


## -description

<p class="CCE_Message">[<b>GetString</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Retrieves the keystroke sequence at the specified index.

## -parameters

### -param uIndex [in]

 The index of the keystroke sequence to retrieve.

### -param pbstr [out]

 The keystroke sequence at the specified index.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The keystroke sequence is stored in <i>pbstr</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The specified index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfreverseconversionlist">ITfReverseConversionList</a>