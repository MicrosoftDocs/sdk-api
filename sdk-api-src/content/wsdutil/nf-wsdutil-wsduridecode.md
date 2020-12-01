---
UID: NF:wsdutil.WSDUriDecode
title: WSDUriDecode function (wsdutil.h)
description: Decodes a URI according to the rules in RFC2396.
helpviewer_keywords: ["WSDUriDecode","WSDUriDecode function","ncd.wsduridecode","wsdutil/WSDUriDecode"]
old-location: ncd\wsduridecode.htm
tech.root: ncd
ms.assetid: 30232a4c-f7bb-4a22-b148-2576a259808a
ms.date: 12/05/2018
ms.keywords: WSDUriDecode, WSDUriDecode function, ncd.wsduridecode, wsdutil/WSDUriDecode
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDUriDecode
 - wsdutil/WSDUriDecode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDUriDecode
---

# WSDUriDecode function


## -description

Decodes a URI according to the rules in RFC2396.

## -parameters

### -param source [in]

Contains the URI to be decoded.

### -param cchSource [in]

Specifies the length of <i>source</i> in characters.

### -param destOut [out]

Pointer to a string that contains the decoded URI.  If <i>destOut</i> is not <b>NULL</b>, the calling application should free the allocated string by calling <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>.

### -param cchDestOut [out, optional]

Specifies the length of <i>destOut</i> in characters.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>source</i> is <b>NULL</b> or <i>cchSource</i> is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>source</i> exceeds <b>WSD_MAX_TEXT_LENGTH</b> (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>destOut</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<b>WSDUriDecode</b> decodes any encoded characters in <i>source</i>.  These characters are identified by a percent sign (%) followed by two hexadecimal digits.  <b>WSDUriDecode</b> decodes single-byte components of multi-byte characters and converts them back to wide character representation in <i>destOut</i>.