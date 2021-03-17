---
UID: NF:wmcontainer.MFCreateASFIndexerByteStream
title: MFCreateASFIndexerByteStream function (wmcontainer.h)
description: Creates a byte stream to access the index in an ASF stream.
helpviewer_keywords: ["MFCreateASFIndexerByteStream","MFCreateASFIndexerByteStream function [Media Foundation]","edcce9d4-9296-4b39-8e58-58ae602c250f","mf.mfcreateasfindexerbytestream","wmcontainer/MFCreateASFIndexerByteStream"]
old-location: mf\mfcreateasfindexerbytestream.htm
tech.root: mf
ms.assetid: edcce9d4-9296-4b39-8e58-58ae602c250f
ms.date: 12/05/2018
ms.keywords: MFCreateASFIndexerByteStream, MFCreateASFIndexerByteStream function [Media Foundation], edcce9d4-9296-4b39-8e58-58ae602c250f, mf.mfcreateasfindexerbytestream, wmcontainer/MFCreateASFIndexerByteStream
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateASFIndexerByteStream
 - wmcontainer/MFCreateASFIndexerByteStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFIndexerByteStream
---

# MFCreateASFIndexerByteStream function


## -description

Creates a byte stream to access the index in an ASF stream.

## -parameters

### -param pIContentByteStream [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream that contains the ASF stream.

### -param cbIndexStartOffset [in]

Byte offset of the index within the ASF stream. To get this value, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition">IMFASFIndexer::GetIndexPosition</a>.

### -param pIIndexByteStream [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface. Use this interface to read from the index or write to the index. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table:

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
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The offset specified in <i>cbIndexStartOffset</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>