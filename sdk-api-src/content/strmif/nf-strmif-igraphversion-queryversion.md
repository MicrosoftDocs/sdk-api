---
UID: NF:strmif.IGraphVersion.QueryVersion
title: IGraphVersion::QueryVersion (strmif.h)
description: The QueryVersion method retrieves the current graph version number.
helpviewer_keywords: ["IGraphVersion interface [DirectShow]","QueryVersion method","IGraphVersion.QueryVersion","IGraphVersion::QueryVersion","IGraphVersionQueryVersion","QueryVersion","QueryVersion method [DirectShow]","QueryVersion method [DirectShow]","IGraphVersion interface","dshow.igraphversion_queryversion","strmif/IGraphVersion::QueryVersion"]
old-location: dshow\igraphversion_queryversion.htm
tech.root: dshow
ms.assetid: 297e19fd-91b5-4756-9b33-6b301c74e470
ms.date: 12/05/2018
ms.keywords: IGraphVersion interface [DirectShow],QueryVersion method, IGraphVersion.QueryVersion, IGraphVersion::QueryVersion, IGraphVersionQueryVersion, QueryVersion, QueryVersion method [DirectShow], QueryVersion method [DirectShow],IGraphVersion interface, dshow.igraphversion_queryversion, strmif/IGraphVersion::QueryVersion
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphVersion::QueryVersion
 - strmif/IGraphVersion::QueryVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphVersion.QueryVersion
---

# IGraphVersion::QueryVersion


## -description

The <code>QueryVersion</code> method retrieves the current graph version number.

## -parameters

### -param pVersion

Pointer to the current graph version.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The version number is incremented every time there is a change in the set of filters in the graph or in their connections. If the version number has changed since the last enumeration, the graph must be re-enumerated.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphversion">IGraphVersion Interface</a>