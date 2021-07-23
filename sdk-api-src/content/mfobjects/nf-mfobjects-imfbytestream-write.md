---
UID: NF:mfobjects.IMFByteStream.Write
title: IMFByteStream::Write (mfobjects.h)
description: Writes data to the stream.
helpviewer_keywords: ["IMFByteStream interface [Media Foundation]","Write method","IMFByteStream.Write","IMFByteStream::Write","Write","Write method [Media Foundation]","Write method [Media Foundation]","IMFByteStream interface","d1f1195a-b6ee-441c-af8b-fce3dc163e95","mf.imfbytestream_write","mfobjects/IMFByteStream::Write"]
old-location: mf\imfbytestream_write.htm
tech.root: mf
ms.assetid: d1f1195a-b6ee-441c-af8b-fce3dc163e95
ms.date: 12/05/2018
ms.keywords: IMFByteStream interface [Media Foundation],Write method, IMFByteStream.Write, IMFByteStream::Write, Write, Write method [Media Foundation], Write method [Media Foundation],IMFByteStream interface, d1f1195a-b6ee-441c-af8b-fce3dc163e95, mf.imfbytestream_write, mfobjects/IMFByteStream::Write
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
 - IMFByteStream::Write
 - mfobjects/IMFByteStream::Write
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
 - IMFByteStream.Write
---

# IMFByteStream::Write


## -description

Writes data to the stream.

## -parameters

### -param pb [in]

Pointer to a buffer that contains the data to write.

### -param cb [in]

Size of the buffer in bytes.

### -param pcbWritten [out]

Receives the number of bytes that are written.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method writes the contents of the <i>pb</i> buffer to the stream, starting at the current stream position. The number of bytes that were written is returned in the <i>pcbWritten</i> parameter.
      

This method is synchronous. It blocks until the write operation completes.
      

<b>Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that were written to the stream, which is specified by the value returned in the <i>pcbWritten</i>, to the current position offset. 

 Other methods that can update the current position are <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read">Read</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread">BeginRead</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">BeginWrite</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">Seek</a>, and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>.


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following example writes data from a media buffer to a byte stream. For more information about media buffers, see <a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>.
        


```cpp
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}

```


The following function template writes a typed variable to a byte stream.


```
template <class T>
HRESULT WriteToStream(
    IMFByteStream *pStream, // Pointer to the byte stream.
    const T* p,             // Data to write to the stream.
    ULONG cb = sizeof(T)    // Size of the data in bytes.
)
{
    ULONG cbWritten = 0;
    HRESULT hr = S_OK;

    hr = pStream->Write((const BYTE*)p, cb, &cbWritten);
    if (SUCCEEDED(hr) && (cbWritten != cb))
    {
        hr = E_FAIL;
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>