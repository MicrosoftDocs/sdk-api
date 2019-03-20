---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.AllocateForStream
title: IWMReaderCallbackAdvanced::AllocateForStream (wmsdkidl.h)
author: windows-sdk-content
description: The AllocateForStream method allocates user-created buffers for stream samples delivered to IWMReaderCallbackAdvanced::OnStreamSample. For more information about allocating your own buffers, see User Allocated Sample Support.
old-location: wmformat\iwmreadercallbackadvanced_allocateforstream.htm
tech.root: wmformat
ms.assetid: 82d31f4b-d8a8-4538-be5e-dd9149e3f420
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AllocateForStream, AllocateForStream method [windows Media Format], AllocateForStream method [windows Media Format],IWMReaderCallbackAdvanced interface, IWMReaderCallbackAdvanced interface [windows Media Format],AllocateForStream method, IWMReaderCallbackAdvanced.AllocateForStream, IWMReaderCallbackAdvanced::AllocateForStream, IWMReaderCallbackAdvancedAllocateForStream, wmformat.iwmreadercallbackadvanced_allocateforstream, wmsdkidl/IWMReaderCallbackAdvanced::AllocateForStream
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMReaderCallbackAdvanced.AllocateForStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderCallbackAdvanced::AllocateForStream


## -description



The <b>AllocateForStream</b> method allocates user-created buffers for stream samples delivered to <a href="https://msdn.microsoft.com/en-us/library/Dd743500(v=VS.85).aspx">IWMReaderCallbackAdvanced::OnStreamSample</a>. For more information about allocating your own buffers, see <a href="https://msdn.microsoft.com/c747139e-e157-4ea0-9132-256dc70e2b15">User Allocated Sample Support</a>.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param cbBuffer [in]

Size of the buffer, in bytes.


### -param ppBuffer [out]

If the method succeeds, returns a pointer to a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd743243(v=VS.85).aspx">INSSBuffer</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://msdn.microsoft.com/en-us/library/Dd743608(v=VS.85).aspx">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/ea1c129b-c0d7-4a1b-934c-c1c07364d4a8">Error Codes</a>.




## -remarks



Stream numbers are in the range of 1 through 63.

An extended version of this method called <a href="https://msdn.microsoft.com/en-us/library/Dd743492(v=VS.85).aspx">AllocateForStreamEx</a> exists in the <a href="https://msdn.microsoft.com/en-us/library/Dd743490(v=VS.85).aspx">IWMReaderAllocatorEx</a> interface.

When allocating buffers, you can use whatever logic suits your application. Typically, applications initialize a pool of buffers for the file or a pool of buffers for each stream or output. When the application is done with a sample, the buffer is put back into the pool for use.

You can determine the size needed to hold the largest sample of an stream by calling <a href="https://msdn.microsoft.com/en-us/library/Dd743474(v=VS.85).aspx">IWMReaderAdvanced::GetMaxStreamSampleSize</a>. This is the size you should make the samples in the pool used for the output.

When you allocate a sample in your implementation of this method, you should call <a href="https://msdn.microsoft.com/en-us/library/Dd743263(v=VS.85).aspx">INSSBuffer::SetLength</a> to set the length of the buffer to the length passed by the reader in the <i>cbBuffer</i> parameter. If you do not set the current length on the buffer, the reader may encounter an error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743494(v=VS.85).aspx">IWMReaderCallbackAdvanced Interface</a>
 

 

