---
UID: NF:strmif.IAsyncReader.Request
title: IAsyncReader::Request
author: windows-sdk-content
description: The Request method queues an asynchronous request for data.
old-location: dshow\iasyncreader_request.htm
tech.root: DirectShow
ms.assetid: d0eab370-bb17-48fa-9926-6a6eeaba5603
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IAsyncReader interface [DirectShow],Request method, IAsyncReader.Request, IAsyncReader::Request, IAsyncReaderRequest, Request, Request method [DirectShow], Request method [DirectShow],IAsyncReader interface, dshow.iasyncreader_request, strmif/IAsyncReader::Request
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAsyncReader.Request
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncReader::Request


## -description



The <code>Request</code> method queues an asynchronous request for data.




## -parameters




### -param pSample

Pointer to the <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface of a media sample provided by the caller.


### -param dwUser [in]

Specifies an arbitrary value that is returned when the request completes.


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
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not aligned correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_SAMPLE_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The sample was not time stamped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pin is flushing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_HANDLE_EOF)</b></dt>
</dl>
</td>
<td width="60%">
The requested start position is past the end of the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, retrieve a media sample from the pin's allocator. Time stamp the sample with the byte offsets you are requesting, first and last inclusive, multiplied by 10,000,000. Byte offsets are relative to the start of the stream.

The start and stop positions should match the alignment that was decided when the pins connected. Otherwise, the method might return VFW_E_BADALIGN. If the agreed alignment is coarser than the actual alignment of the stream, the stop position might exceed the real duration. If so, the method rounds the stop position down to the actual alignment.

Although it is technically a violation of COM rules, the caller must leave an outstanding reference count on the sample. The <code>Request</code> method does not call <b>AddRef</b> or <b>Release</b>, so the reference count is needed to keep the sample active.

The method returns before the request completes. Call the <a href="https://msdn.microsoft.com/fc54f917-3b86-4c0b-b356-217bc9793504">IAsyncReader::WaitForNext</a> method to wait for the request. Do not reuse the original media sample while the request is pending. The <b>WaitForNext</b> method returns a pointer to the original sample. If the request succeeded, the sample contains the requested data. The <b>WaitForNext</b> method also returns whatever value is specified in the <i>dwUser</i> parameter. The caller can use this value to identify the sample.


#### Examples

The following example shows a possible helper function for an input pin, to queue requests:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CMyPin::QueueSample(long cbFirst, long cbLast, DWORD_PTR dwuser)
{
    IMediaSample* pSample = NULL;
    HRESULT hr = m_pAlloc-&gt;GetBuffer(&amp;pSample, NULL, NULL, 0);
    if (FAILED(hr)) 
    { 
        return hr; 
    }

    LONGLONG tStart = cbFirst * 10000000, tStop = cbLast * 10000000;
    hr = pSample-&gt;SetTime(&amp;tStart, &amp;tStop);
    if (SUCCEEDED(hr))
    {
        hr = m_pReader-&gt;Request(pSample, dwuser);
    }

    if (FAILED(hr))
    {
        pSample-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>
 

 

