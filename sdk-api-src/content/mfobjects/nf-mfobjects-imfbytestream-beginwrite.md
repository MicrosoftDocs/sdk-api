---
UID: NF:mfobjects.IMFByteStream.BeginWrite
title: IMFByteStream::BeginWrite
author: windows-sdk-content
description: Begins an asynchronous write operation to the stream.
old-location: mf\imfbytestream_beginwrite.htm
tech.root: medfound
ms.assetid: 078a8ffe-7b4f-487e-8655-fe5ea14ba306
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 078a8ffe-7b4f-487e-8655-fe5ea14ba306, BeginWrite, BeginWrite method [Media Foundation], BeginWrite method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],BeginWrite method, IMFByteStream.BeginWrite, IMFByteStream::BeginWrite, mf.imfbytestream_beginwrite, mfobjects/IMFByteStream::BeginWrite
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
 - IMFByteStream.BeginWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStream::BeginWrite


## -description


Begins an asynchronous write operation to the stream.
        


## -parameters




### -param pb [in]

Pointer to a buffer containing the data to write.
          


### -param cb [in]

Size of the buffer in bytes.
          


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When all of the data has been written to the stream, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/d3e10e89-ef5d-41c5-b549-4bd632d9370d">IMFByteStream::EndWrite</a> to complete the asynchronous request.
      

Do not reallocate, free, or write to the buffer while an asynchronous write is still pending.
      

<b>Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that will be written to the stream, which is specified by the value returned in the <i>pcbWritten</i>, to the current position. Other methods that can update the current position are <a href="https://msdn.microsoft.com/6e0d5363-f2c2-4334-86ca-71fac61073d3">Read</a>, <a href="https://msdn.microsoft.com/ed4aaf2a-270c-4518-b04d-cdac966bf9a5">BeginRead</a>, <a href="https://msdn.microsoft.com/d1f1195a-b6ee-441c-af8b-fce3dc163e95">Write</a>, <a href="https://msdn.microsoft.com/512c67a5-e87d-4a81-8577-e64dac868c40">Seek</a>, and <a href="https://msdn.microsoft.com/20518fed-4083-413b-b9b1-e54c4c5630d4">SetCurrentPosition</a>.


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

