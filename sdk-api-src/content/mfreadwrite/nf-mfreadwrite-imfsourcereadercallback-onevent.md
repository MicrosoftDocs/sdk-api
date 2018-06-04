---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

