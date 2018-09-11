---
UID: NF:mfobjects.IMFByteStream.EndWrite
title: IMFByteStream::EndWrite
author: windows-sdk-content
description: Completes an asynchronous write operation.
old-location: mf\imfbytestream_endwrite.htm
tech.root: medfound
ms.assetid: d3e10e89-ef5d-41c5-b549-4bd632d9370d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EndWrite, EndWrite method [Media Foundation], EndWrite method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],EndWrite method, IMFByteStream.EndWrite, IMFByteStream::EndWrite, d3e10e89-ef5d-41c5-b549-4bd632d9370d, mf.imfbytestream_endwrite, mfobjects/IMFByteStream::EndWrite
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
 - IMFByteStream.EndWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStream::EndWrite


## -description



Completes an asynchronous write operation.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


### -param pcbWritten [out]

Receives the number of bytes that were written.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method when the <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">IMFByteStream::BeginWrite</a> method completes asynchronously.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

