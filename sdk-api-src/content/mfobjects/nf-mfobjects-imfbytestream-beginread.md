---
UID: NF:mfobjects.IMFByteStream.BeginRead
title: IMFByteStream::BeginRead
author: windows-driver-content
description: Begins an asynchronous read operation from the stream.
old-location: mf\imfbytestream_beginread.htm
old-project: medfound
ms.assetid: ed4aaf2a-270c-4518-b04d-cdac966bf9a5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: BeginRead, BeginRead method [Media Foundation], BeginRead method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],BeginRead method, IMFByteStream.BeginRead, IMFByteStream::BeginRead, ed4aaf2a-270c-4518-b04d-cdac966bf9a5, mf.imfbytestream_beginread, mfobjects/IMFByteStream::BeginRead
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFByteStream.BeginRead
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStream::BeginRead


## -description



          Begins an asynchronous read operation from the stream.
        


## -parameters




### -param pb [in]


            Pointer to a buffer that receives the data. The caller must allocate the buffer.
          


### -param cb [in]


            Size of the buffer in bytes.
          


### -param pCallback [in]


            Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param punkState [in]


            Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        When all of the data has been read into the buffer, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/dd62f644-fb97-474b-8303-3086a7b51c4d">IMFByteStream::EndRead</a> to complete the asynchronous request.
      


        Do not read from, write to, free, or reallocate the buffer while an asynchronous read is pending.
      

<b> Implementation notes:</b>
This method should update the current position in the stream by adding the number of bytes that will be read, which is specified by the value returned in the <i>pcbRead</i> parameter,  to the current position. Other methods that can update the current position are <b>BeginRead</b>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>, <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">BeginWrite</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/20518fed-4083-413b-b9b1-e54c4c5630d4">SetCurrentPosition</a>. 


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

