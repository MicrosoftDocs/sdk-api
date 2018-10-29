---
UID: NF:mfobjects.IMFByteStream.Write
title: IMFByteStream::Write
author: windows-sdk-content
description: Writes data to the stream.
old-location: mf\imfbytestream_write.htm
tech.root: medfound
ms.assetid: d1f1195a-b6ee-441c-af8b-fce3dc163e95
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFByteStream interface [Media Foundation],Write method, IMFByteStream.Write, IMFByteStream::Write, Write, Write method [Media Foundation], Write method [Media Foundation],IMFByteStream interface, d1f1195a-b6ee-441c-af8b-fce3dc163e95, mf.imfbytestream_write, mfobjects/IMFByteStream::Write
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
 - IMFByteStream.Write
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method writes the contents of the <i>pb</i> buffer to the stream, starting at the current stream position. The number of bytes that were written is returned in the <i>pcbWritten</i> parameter.
      

This method is synchronous. It blocks until the write operation completes.
      

<b>Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that were written to the stream, which is specified by the value returned in the <i>pcbWritten</i>, to the current position offset. 

 Other methods that can update the current position are <a href="https://msdn.microsoft.com/6e0d5363-f2c2-4334-86ca-71fac61073d3">Read</a>, <a href="https://msdn.microsoft.com/ed4aaf2a-270c-4518-b04d-cdac966bf9a5">BeginRead</a>, <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">BeginWrite</a>, <a href="https://msdn.microsoft.com/512c67a5-e87d-4a81-8577-e64dac868c40">Seek</a>, and <a href="https://msdn.microsoft.com/20518fed-4083-413b-b9b1-e54c4c5630d4">SetCurrentPosition</a>.


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples

The following example writes data from a media buffer to a byte stream. For more information about media buffers, see <a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>.
        


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




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

