---
UID: NF:mfobjects.IMFSampleOutputStream.EndWriteSample
title: IMFSampleOutputStream::EndWriteSample (mfobjects.h)
author: windows-sdk-content
description: Completes an asynchronous request to write a media sample to the stream.
old-location: mf\imfsampleoutputstream_endwritesample.htm
tech.root: medfound
ms.assetid: AE65CE63-B7FF-403B-ABB8-5E6C53CAD314
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndWriteSample, EndWriteSample method [Media Foundation], EndWriteSample method [Media Foundation],IMFSampleOutputStream interface, IMFSampleOutputStream interface [Media Foundation],EndWriteSample method, IMFSampleOutputStream.EndWriteSample, IMFSampleOutputStream::EndWriteSample, mf.imfsampleoutputstream_endwritesample, mfobjects/IMFSampleOutputStream::EndWriteSample
ms.topic: method
f1_keywords: ["mfobjects/IMFSampleOutputStream.EndWriteSample"]
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfobjects.h
api_name:
 - IMFSampleOutputStream.EndWriteSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSampleOutputStream::EndWriteSample


## -description


Completes an asynchronous request to write a media sample to the stream.


## -parameters




### -param pResult [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method when the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-beginwritesample">IMFSampleOutputStream::BeginWriteSample</a> method completes asynchronously. 






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream">IMFSampleOutputStream</a>
 

 

