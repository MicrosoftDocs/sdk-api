---
UID: NF:wmcontainer.IMFASFIndexer.GetCompletedIndex
title: IMFASFIndexer::GetCompletedIndex
author: windows-sdk-content
description: Retrieves the completed index from the ASF indexer object.
old-location: mf\imfasfindexer_getcompletedindex.htm
old-project: medfound
ms.assetid: aca721e8-e610-4022-a3da-8ff5a5943e3e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCompletedIndex, GetCompletedIndex method [Media Foundation], GetCompletedIndex method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetCompletedIndex method, IMFASFIndexer.GetCompletedIndex, IMFASFIndexer::GetCompletedIndex, aca721e8-e610-4022-a3da-8ff5a5943e3e, mf.imfasfindexer_getcompletedindex, wmcontainer/IMFASFIndexer::GetCompletedIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFIndexer.GetCompletedIndex
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::GetCompletedIndex


## -description



Retrieves the completed index from the ASF indexer object.




## -parameters




### -param pIIndexBuffer [in]

Pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of a media buffer that receives the index data.


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

The user must write this data to the content at <i>cbOffsetFromIndexStart</i> bytes after the end of the ASF data object. You can call <a href="https://msdn.microsoft.com/7ef0e36c-1be5-44ac-8f6a-e29805c99e78">IMFASFIndexer::GetIndexPosition</a> to determine the start position of the ASF index.

This call will not succeed unless <a href="https://msdn.microsoft.com/44b889e1-8860-44fa-b19f-5be9f844a194">IMFASFIndexer::CommitIndex</a> has been called. After calling <b>GetCompletedIndex</b>, the caller must call <a href="https://msdn.microsoft.com/972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e">IMFASFContentInfo::GenerateHeader</a> and overwrite the existing ASF header with the new header; otherwise, the ASF header will not match the content, and the file is not guaranteed to play correctly.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.


#### Examples

The following example shows how to write the complete ASF index to a byte stream.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex-&gt;GetIndexWriteSpace(&amp;cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &amp;pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten &lt; cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex-&gt;GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer-&gt;Lock(&amp;pData, NULL, &amp;cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream-&gt;Write(pData, cbData, &amp;cbWritten);

        (void)pBuffer-&gt;Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&amp;pBuffer);
    return hr;
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>



<a href="https://msdn.microsoft.com/a14e3bef-0232-4259-930a-d860ed9230fd">Using the Indexer to Write a New Index</a>
 

 

