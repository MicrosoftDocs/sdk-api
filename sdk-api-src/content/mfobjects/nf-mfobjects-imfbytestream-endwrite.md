---
UID: NF:mfobjects.IMFByteStream.EndWrite
title: IMFByteStream::EndWrite (mfobjects.h)
description: Completes an asynchronous write operation.
helpviewer_keywords: ["EndWrite","EndWrite method [Media Foundation]","EndWrite method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","EndWrite method","IMFByteStream.EndWrite","IMFByteStream::EndWrite","d3e10e89-ef5d-41c5-b549-4bd632d9370d","mf.imfbytestream_endwrite","mfobjects/IMFByteStream::EndWrite"]
old-location: mf\imfbytestream_endwrite.htm
tech.root: medfound
ms.assetid: d3e10e89-ef5d-41c5-b549-4bd632d9370d
ms.date: 12/05/2018
ms.keywords: EndWrite, EndWrite method [Media Foundation], EndWrite method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],EndWrite method, IMFByteStream.EndWrite, IMFByteStream::EndWrite, d3e10e89-ef5d-41c5-b549-4bd632d9370d, mf.imfbytestream_endwrite, mfobjects/IMFByteStream::EndWrite
f1_keywords:
- mfobjects/IMFByteStream.EndWrite
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStream::EndWrite


## -description



Completes an asynchronous write operation.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.


### -param pcbWritten [out]

Receives the number of bytes that were written.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method when the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">IMFByteStream::BeginWrite</a> method completes asynchronously.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>
 

 

