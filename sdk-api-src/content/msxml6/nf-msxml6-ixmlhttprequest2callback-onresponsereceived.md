---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnResponseReceived
title: IXMLHTTPRequest2Callback::OnResponseReceived method
author: windows-driver-content
description: Occurs when a client has received a complete response from the server.
old-location: ixhr2\ixmlhttprequest2callback_onresponsereceived.htm
old-project: ixhr2
ms.assetid: 5D1D4D4B-CC49-4A63-A0D5-B29D618E80DE
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IXMLHTTPRequest2Callback, IXMLHTTPRequest2Callback interface [XMLHttpRequest2], OnResponseReceived method, IXMLHTTPRequest2Callback::OnResponseReceived, OnResponseReceived method [XMLHttpRequest2], OnResponseReceived method [XMLHttpRequest2], IXMLHTTPRequest2Callback interface, OnResponseReceived,IXMLHTTPRequest2Callback.OnResponseReceived, ixhr2.ixmlhttprequest2callback_onresponsereceived, msxml6/IXMLHTTPRequest2Callback::OnResponseReceived
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XHR_PROPERTY, XHR_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msxml6.h
api_name:
-	IXMLHTTPRequest2Callback.OnResponseReceived
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IXMLHTTPRequest2Callback::OnResponseReceived method


## -description


Occurs when a client has received a complete response from the server.


## -parameters




### -param pXHR [in, optional]

The initial HTTP request object


### -param pResponseStream [in, optional]

The response stream being received. The client can call <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> to begin processing the data, or it can store a reference to <i>pResponseStream</i> for later processing. This response stream is wrapped in a stream synchronization object that prevents concurrent read and write operations, so the application does not need to implement custom synchronization.


## -returns



Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>



## -remarks



When this event fires the application can begin processing data from the HTTP response. Processing may begin before this event fires if an earlier <a href="https://msdn.microsoft.com/068C3288-A872-43FA-BF1F-D7A3CD2E2203">OnDataAvailable</a> event has occurred.



Unless <a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a> is called, the call to <b>OnResponseReceived</b> is the final callback. The client should perform any required cleanup including releasing references to the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> object.

Custom streams receive a call to <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> specifying 0 bytes written before <b>OnResponseReceived</b> is fired. The client can process data directly from the Write call instead of calling <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> on the custom stream, and it can rely on the zero-byte Write call to indicate that the response has been received.




## -see-also




<a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream Interface</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>
 

 

