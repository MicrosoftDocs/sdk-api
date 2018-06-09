---
UID: NF:msxml6.IXMLHTTPRequest2.Send
title: IXMLHTTPRequest2::Send
author: windows-sdk-content
description: Sends an HTTP request to the server asynchronously. On success, methods on the IXMLHTTPRequest2Callback interface implemented by the app are called to process the response.
old-location: ixhr2\ixmlhttprequest2_send.htm
old-project: ixhr2
ms.assetid: E46DB550-8346-41F2-9B35-4DFD9732B0D8
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],Send method, IXMLHTTPRequest2.Send, IXMLHTTPRequest2::Send, Send, Send method [XMLHttpRequest2], Send method [XMLHttpRequest2],IXMLHTTPRequest2 interface, ixhr2.ixmlhttprequest2_send, msxml6/IXMLHTTPRequest2::Send
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XHR_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.Send
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest2::Send


## -description


Sends an HTTP request to the server asynchronously. On success, methods on the <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> interface implemented by the app are called to process the response.


## -parameters




### -param pBody [in, optional]

The body of the message being sent with the request. This stream is read in order to upload data for non-<b>GET</b> requests. For requests that do not require uploading, set this parameter to NULL.


### -param cbBody [in]

The length, in bytes, of the message being sent with the request. For requests that do not require uploading, set this parameter to 0.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> method must be called before <b>Send</b> can be called successfully.

Because this method is asynchronous, it returns immediately before the request has started processing.  The application will be notified through the <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> interface as progress is made in the request processing.

Alternatives to using <a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream</a>  for a POST request include <a href="https://msdn.microsoft.com/f3ae8241-f3a6-4007-a10f-ff05960c5de8">SHCreateMemStream</a>/<a href="https://msdn.microsoft.com/9b1fd6c4-d7b0-40b9-bc9f-ea062a1079c1">SHCreateStreamOnFile</a> for desktop apps, and <a href="https://msdn.microsoft.com/F9AB8A34-8AB1-4EF1-8659-DAD5713A89BF">CreateStreamOverRandomAccessStream</a> for Windows Store apps.




## -see-also




<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>
 

 

