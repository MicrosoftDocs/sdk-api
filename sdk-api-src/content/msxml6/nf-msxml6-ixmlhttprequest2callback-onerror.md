---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnError
title: IXMLHTTPRequest2Callback::OnError
author: windows-sdk-content
description: Occurs when an error is encountered or the request has been aborted.
old-location: ixhr2\ixmlhttprequest2callback_onerror.htm
old-project: ixhr2
ms.assetid: 532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnError method, IXMLHTTPRequest2Callback.OnError, IXMLHTTPRequest2Callback::OnError, OnError, OnError method [XMLHttpRequest2], OnError method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onerror, msxml6/IXMLHTTPRequest2Callback::OnError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IXMLHTTPRequest2Callback.OnError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest2Callback::OnError


## -description


Occurs when an error is encountered or the request has been aborted.


## -parameters




### -param pXHR [in, optional]

The initial HTTP request.


### -param hrError

A code representing the error that occurred on the HTTP request.


## -returns



Returns<b> S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>



## -remarks



Unless the request completes successfully, indicated by <a href="https://msdn.microsoft.com/5D1D4D4B-CC49-4A63-A0D5-B29D618E80DE">OnResponseReceived</a>, the call to <b>OnError</b> is the final callback. The client should perform any required cleanup including releasing references to the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> object.




## -see-also




<a href="https://msdn.microsoft.com/c1d33800-d2f1-4942-92fa-e115f524c23c">ISequentialStream Interface</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>
 

 

