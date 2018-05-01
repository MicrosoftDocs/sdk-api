---
UID: NF:mfobjects.IMFSampleOutputStream.BeginWriteSample
title: IMFSampleOutputStream::BeginWriteSample method
author: windows-driver-content
description: Begins an asynchronous request to write a media sample to the stream.
old-location: mf\imfsampleoutputstream_beginwritesample.htm
old-project: medfound
ms.assetid: 41056795-3E12-448E-9341-FB4DD4E7D079
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: BeginWriteSample method [Media Foundation], BeginWriteSample method [Media Foundation], IMFSampleOutputStream interface, BeginWriteSample,IMFSampleOutputStream.BeginWriteSample, IMFSampleOutputStream, IMFSampleOutputStream interface [Media Foundation], BeginWriteSample method, IMFSampleOutputStream::BeginWriteSample, mf.imfsampleoutputstream_beginwritesample, mfobjects/IMFSampleOutputStream::BeginWriteSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
-	mfobjects.h
api_name:
-	IMFSampleOutputStream.BeginWriteSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSampleOutputStream::BeginWriteSample method


## -description


Begins an asynchronous request to write a media sample to the stream.


## -parameters




### -param pSample [in]

A pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the sample.


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param punkState [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked. 




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the sample has been written to the stream, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the caller should call <a href="https://msdn.microsoft.com/AE65CE63-B7FF-403B-ABB8-5E6C53CAD314">IMFSampleOutputStream::EndWriteSample</a> to complete the asynchronous request. 






## -see-also




<a href="https://msdn.microsoft.com/BA293BB7-9191-4123-96DB-FF6386ABB3AE">IMFSampleOutputStream</a>
 

 

