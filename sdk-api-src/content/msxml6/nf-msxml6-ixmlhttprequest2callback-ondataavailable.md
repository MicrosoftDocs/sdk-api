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

# IXMLHTTPRequest2Callback::OnDataAvailable


## -description


Occurs when a client receives part of the HTTP response data from the server.


## -parameters




### -param pXHR [in, optional]

The initial HTTP request.


### -param pResponseStream [in, optional]

The response stream being received. The client can call <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> to begin processing the data, or it can wait until it has received the complete response. This response stream is wrapped in a stream synchronization object that prevents concurrent read and write operations, so the application does not need to implement custom synchronization.


## -returns



Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>



## -remarks



When this callback function returns  the application can begin processing data from the HTTP response, even if it has not yet received the entire response. However, receiving is suspended for the request until this callback function returns. Additionally, this callback can be  invoked multiple times during a single request.

This callback function must not block and should not be made to perform resource intensive operations such as UI updates.

Custom streams receive a call to <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> before <b>OnDataAvailable</b> is fired. The client can process data directly from the Write call instead of calling <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> on the custom stream, and it can rely on the Write call to indicate that new data is available.





## -see-also




<a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream Interface</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>
 

 

