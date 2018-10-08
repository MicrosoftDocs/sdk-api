---
UID: NF:mfobjects.IMFSampleOutputStream.EndWriteSample
title: IMFSampleOutputStream::EndWriteSample
author: windows-sdk-content
description: Completes an asynchronous request to write a media sample to the stream.
old-location: mf\imfsampleoutputstream_endwritesample.htm
tech.root: medfound
ms.assetid: AE65CE63-B7FF-403B-ABB8-5E6C53CAD314
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: EndWriteSample, EndWriteSample method [Media Foundation], EndWriteSample method [Media Foundation],IMFSampleOutputStream interface, IMFSampleOutputStream interface [Media Foundation],EndWriteSample method, IMFSampleOutputStream.EndWriteSample, IMFSampleOutputStream::EndWriteSample, mf.imfsampleoutputstream_endwritesample, mfobjects/IMFSampleOutputStream::EndWriteSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IMFSampleOutputStream::EndWriteSample


## -description


Completes an asynchronous request to write a media sample to the stream.


## -parameters




### -param pResult [in]

A pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method when the <a href="https://msdn.microsoft.com/41056795-3E12-448E-9341-FB4DD4E7D079">IMFSampleOutputStream::BeginWriteSample</a> method completes asynchronously. 






## -see-also




<a href="https://msdn.microsoft.com/BA293BB7-9191-4123-96DB-FF6386ABB3AE">IMFSampleOutputStream</a>
 

 

