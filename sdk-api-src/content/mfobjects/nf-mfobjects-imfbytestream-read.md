---
UID: NF:mfobjects.IMFByteStream.Read
title: IMFByteStream::Read (mfobjects.h)
description: Reads data from the stream.
helpviewer_keywords: ["6e0d5363-f2c2-4334-86ca-71fac61073d3","IMFByteStream interface [Media Foundation]","Read method","IMFByteStream.Read","IMFByteStream::Read","Read","Read method [Media Foundation]","Read method [Media Foundation]","IMFByteStream interface","mf.imfbytestream_read","mfobjects/IMFByteStream::Read"]
old-location: mf\imfbytestream_read.htm
tech.root: mf
ms.assetid: 6e0d5363-f2c2-4334-86ca-71fac61073d3
ms.date: 12/05/2018
ms.keywords: 6e0d5363-f2c2-4334-86ca-71fac61073d3, IMFByteStream interface [Media Foundation],Read method, IMFByteStream.Read, IMFByteStream::Read, Read, Read method [Media Foundation], Read method [Media Foundation],IMFByteStream interface, mf.imfbytestream_read, mfobjects/IMFByteStream::Read
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStream::Read
 - mfobjects/IMFByteStream::Read
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
 - IMFByteStream.Read
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method reads at most <i>cb</i> bytes from the current position in the stream and copies them into the buffer provided by the caller. The number of bytes that were read is returned in the <i>pcbRead</i> parameter. The method does not return an error code on reaching the end of the file, so the application should check the value in <i>pcbRead</i> after the method returns.
      

This method is synchronous. It blocks until the read operation completes.
      

<b> Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that were read, which is specified by the value returned in the <i>pcbRead</i> parameter,  to the current position. Other methods that can update the current position are <b>Read</b>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write">Write</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">BeginWrite</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">Seek</a>, and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>. 


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following example reads data from a byte stream into a caller-allocated media buffer. For more information about media buffers, see <a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>. 


```cpp
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size of the 
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

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}

```


The next example is similar, but allocates a new media buffer to hold the data. 


<div class="alert"><b>Note</b>  This example uses the <a href="/windows/desktop/medfound/saferelease">SafeRelease</a> function to release interface pointers.</div>
<div> </div>



```cpp
//-------------------------------------------------------------------
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
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>