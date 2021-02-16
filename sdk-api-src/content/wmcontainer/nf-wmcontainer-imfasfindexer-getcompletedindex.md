---
UID: NF:wmcontainer.IMFASFIndexer.GetCompletedIndex
title: IMFASFIndexer::GetCompletedIndex (wmcontainer.h)
description: Retrieves the completed index from the ASF indexer object.
helpviewer_keywords: ["GetCompletedIndex","GetCompletedIndex method [Media Foundation]","GetCompletedIndex method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetCompletedIndex method","IMFASFIndexer.GetCompletedIndex","IMFASFIndexer::GetCompletedIndex","aca721e8-e610-4022-a3da-8ff5a5943e3e","mf.imfasfindexer_getcompletedindex","wmcontainer/IMFASFIndexer::GetCompletedIndex"]
old-location: mf\imfasfindexer_getcompletedindex.htm
tech.root: medfound
ms.assetid: aca721e8-e610-4022-a3da-8ff5a5943e3e
ms.date: 12/05/2018
ms.keywords: GetCompletedIndex, GetCompletedIndex method [Media Foundation], GetCompletedIndex method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetCompletedIndex method, IMFASFIndexer.GetCompletedIndex, IMFASFIndexer::GetCompletedIndex, aca721e8-e610-4022-a3da-8ff5a5943e3e, mf.imfasfindexer_getcompletedindex, wmcontainer/IMFASFIndexer::GetCompletedIndex
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFIndexer::GetCompletedIndex
 - wmcontainer/IMFASFIndexer::GetCompletedIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFIndexer.GetCompletedIndex
---

# IMFASFIndexer::GetCompletedIndex


## -description

Retrieves the completed index from the ASF indexer object.

## -parameters

### -param pIIndexBuffer [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of a media buffer that receives the index data.

### -param cbOffsetWithinIndex [in]

The offset of the data to be retrieved, in bytes from the start of the index data. Set to 0 for the first call. If subsequent calls are needed (the buffer is not large enough to hold the entire index), set to the byte following the last one retrieved.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INDEX_NOT_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
The index was not committed before attempting to get the completed index. For more information, see Remarks.

</td>
</tr>
</table>

## -remarks

This method uses as much of the buffer as possible, and updates the length of the buffer appropriately.

If <i>pIIndexBuffer</i> is large enough to contain the entire buffer, <i>cbOffsetWithinIndex</i> should be 0, and the call needs to be made only once. Otherwise, there should be no gaps between successive buffers.

The user must write this data to the content at <i>cbOffsetFromIndexStart</i> bytes after the end of the ASF data object. You can call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition">IMFASFIndexer::GetIndexPosition</a> to determine the start position of the ASF index.

This call will not succeed unless <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex">IMFASFIndexer::CommitIndex</a> has been called. After calling <b>GetCompletedIndex</b>, the caller must call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader">IMFASFContentInfo::GenerateHeader</a> and overwrite the existing ASF header with the new header; otherwise, the ASF header will not match the content, and the file is not guaranteed to play correctly.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.


#### Examples

The following example shows how to write the complete ASF index to a byte stream.


```cpp
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};

```

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>



<a href="/previous-versions/windows/desktop/legacy/dd757932(v=vs.85)">Using the Indexer to Write a New Index</a>