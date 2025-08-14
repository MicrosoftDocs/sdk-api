---
UID: NF:combaseapi.CoUnmarshalHresult
title: CoUnmarshalHresult function (combaseapi.h)
description: Unmarshals an HRESULT type from the specified stream.
helpviewer_keywords: ["CoUnmarshalHresult","CoUnmarshalHresult function [COM]","_com_CoUnmarshalHresult","com.counmarshalhresult","combaseapi/CoUnmarshalHresult"]
old-location: com\counmarshalhresult.htm
tech.root: com
ms.assetid: a45ef72c-d385-4012-9683-7d2cc6d68b6d
ms.date: 12/05/2018
ms.keywords: CoUnmarshalHresult, CoUnmarshalHresult function [COM], _com_CoUnmarshalHresult, com.counmarshalhresult, combaseapi/CoUnmarshalHresult
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoUnmarshalHresult
 - combaseapi/CoUnmarshalHresult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoUnmarshalHresult
---

# CoUnmarshalHresult function


## -description

Unmarshals an <b>HRESULT</b> type from the specified stream.

## -parameters

### -param pstm [in]

A pointer to the stream from which the <b>HRESULT</b> is to be unmarshaled.

### -param phresult [out]

A pointer to the unmarshaled <b>HRESULT</b>.

## -returns

This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The <b>HRESULT</b> was unmarshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pStm</i> is an invalid pointer.


</td>
</tr>
</table>

## -remarks

You do not explicitly call this function unless you are performing custom marshaling (that is, writing your own implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>), and your implementation needs to unmarshal an <b>HRESULT</b>.

You must use <b>CoUnmarshalHresult</b> to unmarshal <b>HRESULT</b> values previously marshaled by a call to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalhresult">CoMarshalHresult</a> function.

This function performs the following tasks:

<ol>
<li>
 an <b>HRESULT</b> from a stream.

</li>
<li>Returns the <b>HRESULT</b>.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalhresult">CoMarshalHresult</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>