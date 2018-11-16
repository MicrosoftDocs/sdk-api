---
UID: NF:mfobjects.IMFByteStream.Read
title: IMFByteStream::Read
author: windows-sdk-content
description: Reads data from the stream.
old-location: mf\imfbytestream_read.htm
tech.root: medfound
ms.assetid: 6e0d5363-f2c2-4334-86ca-71fac61073d3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 6e0d5363-f2c2-4334-86ca-71fac61073d3, IMFByteStream interface [Media Foundation],Read method, IMFByteStream.Read, IMFByteStream::Read, Read, Read method [Media Foundation], Read method [Media Foundation],IMFByteStream interface, mf.imfbytestream_read, mfobjects/IMFByteStream::Read
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream.Read
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfobjects.h
: 
- IMFByteStream.Read
: 
---

# IMFByteStream::Read


## -description


Reads data from the stream.
        


## -parameters




### -param pb [in]

Pointer to a buffer that receives the data. The caller must allocate the buffer.
          


### -param cb [in]

Size of the buffer in bytes.
          


### -param pcbRead [out]

Receives the number of bytes that are copied into the buffer. This parameter cannot be <b>NULL</b>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method reads at most <i>cb</i> bytes from the current position in the stream and copies them into the buffer provided by the caller. The number of bytes that were read is returned in the <i>pcbRead</i> parameter. The method does not return an error code on reaching the end of the file, so the application should check the value in <i>pcbRead</i> after the method returns.
      

This method is synchronous. It blocks until the read operation completes.
      

<b> Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that were read, which is specified by the value returned in the <i>pcbRead</i> parameter,  to the current position. Other methods that can update the current position are <b>Read</b>, <a href="https://msdn.microsoft.com/d1f1195a-b6ee-441c-af8b-fce3dc163e95">Write</a>, <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">BeginWrite</a>, <a href="https://msdn.microsoft.com/512c67a5-e87d-4a81-8577-e64dac868c40">Seek</a>, and <a href="https://msdn.microsoft.com/20518fed-4083-413b-b9b1-e54c4c5630d4">SetCurrentPosition</a>. 


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following example reads data from a byte stream into a caller-allocated media buffer. For more information about media buffers, see <a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer-&gt;Lock(&amp;pData, &amp;cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax &gt; cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream-&gt;Read(pData, cbMax, &amp;cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer-&gt;SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer-&gt;Unlock();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
The next example is similar, but allocates a new media buffer to hold the data. 


<div class="alert"><b>Note</b>  This example uses the <a href="https://msdn.microsoft.com/2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75">SafeRelease</a> function to release interface pointers.</div>
<div> </div>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &amp;pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer-&gt;Lock(&amp;pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream-&gt;Read(pData, cbToRead, &amp;cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer-&gt;SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)-&gt;AddRef();
    }

    if (pData)
    {
        pBuffer-&gt;Unlock();
    }
    SafeRelease(&amp;pBuffer);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

