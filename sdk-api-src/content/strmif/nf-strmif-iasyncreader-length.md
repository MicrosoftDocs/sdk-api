---
UID: NF:strmif.IAsyncReader.Length
title: IAsyncReader::Length (strmif.h)
description: The Length method retrieves the total length of the stream.
helpviewer_keywords: ["IAsyncReader interface [DirectShow]","Length method","IAsyncReader.Length","IAsyncReader::Length","IAsyncReaderLength","Length","Length method [DirectShow]","Length method [DirectShow]","IAsyncReader interface","dshow.iasyncreader_length","strmif/IAsyncReader::Length"]
old-location: dshow\iasyncreader_length.htm
tech.root: dshow
ms.assetid: 4e583ade-92a9-4853-96fb-c46cd24dd7ac
ms.date: 12/05/2018
ms.keywords: IAsyncReader interface [DirectShow],Length method, IAsyncReader.Length, IAsyncReader::Length, IAsyncReaderLength, Length, Length method [DirectShow], Length method [DirectShow],IAsyncReader interface, dshow.iasyncreader_length, strmif/IAsyncReader::Length
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
 - IAsyncReader::Length
 - strmif/IAsyncReader::Length
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
 - IAsyncReader.Length
---

# IAsyncReader::Length


## -description

The <code>Length</code> method retrieves the total length of the stream.

## -parameters

### -param pTotal

Pointer to a variable that receives the length of the stream, in bytes.

### -param pAvailable

Pointer to a variable that receives the portion of the stream that is currently available, in bytes.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_ESTIMATED</b></dt>
</dl>
</td>
<td width="60%">
The returned values are estimates; for example, if the file is being read over a network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The file is not open or no longer exists.

</td>
</tr>
</table>

## -remarks

For streams retrieved over a network, the entire stream may not be available at first. Read operations beyond the available length might block for a long period of time, until that portion of the stream becomes available.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>