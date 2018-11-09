---
UID: NF:mfreadwrite.IMFSourceReaderCallback.OnEvent
title: IMFSourceReaderCallback::OnEvent
author: windows-sdk-content
description: Called when the source reader receives certain events from the media source.
old-location: mf\imfsourcereadercallback_onevent.htm
tech.root: medfound
ms.assetid: cbe85d0f-26a1-4526-bfe6-b6183812a271
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFSourceReaderCallback interface [Media Foundation],OnEvent method, IMFSourceReaderCallback.OnEvent, IMFSourceReaderCallback::OnEvent, OnEvent, OnEvent method [Media Foundation], OnEvent method [Media Foundation],IMFSourceReaderCallback interface, mf.imfsourcereadercallback_onevent, mfreadwrite/IMFSourceReaderCallback::OnEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback.OnEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReaderCallback::OnEvent


## -description


Called when the source reader receives certain events from the media source.


## -parameters




### -param dwStreamIndex [in]

For stream events, the value is the zero-based index of the stream that sent the event. For source events, the value is <b>MF_SOURCE_READER_MEDIASOURCE</b>.


### -param pEvent [in]

A pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface of the event.


## -returns



Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.




## -remarks



In the current implementation,  the source reader uses this method to forward the following events to the application:

<ul>
<li>
<a href="https://msdn.microsoft.com/8637dfcd-2e0c-4cf4-a216-4089c201bfc6">MEBufferingStarted</a>
</li>
<li>
<a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a>
</li>
<li>
<a href="https://msdn.microsoft.com/737aec32-24f4-4825-ad34-8d2fc889bc09">MEConnectEnd</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0844ac10-cc5b-4e7f-92df-3a5901c72148">MEConnectStart</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a54a446c-0e96-467b-90f6-0f64a7c1727d">MEExtendedType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3">MESourceCharacteristicsChanged</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6818b0c9-9628-41e6-8dc6-dff26f4fcfd2">MESourceMetadataChanged</a>
</li>
</ul>
This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/fff8b6e6-5d56-4301-b3ce-f3ff49398593">IMFSourceReaderCallback</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

