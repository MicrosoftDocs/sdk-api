---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnRedirect
title: IXMLHTTPRequest2Callback::OnRedirect
author: windows-driver-content
description: Occurs when a client sends an HTTP request that the server redirects to a new URL.
old-location: ixhr2\ixmlhttprequest2callback_onredirect.htm
old-project: ixhr2
ms.assetid: 8492FFD5-99C8-4545-B5FD-465CC01D0038
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnRedirect method, IXMLHTTPRequest2Callback.OnRedirect, IXMLHTTPRequest2Callback::OnRedirect, OnRedirect, OnRedirect method [XMLHttpRequest2], OnRedirect method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onredirect, msxml6/IXMLHTTPRequest2Callback::OnRedirect
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
req.typenames: XHR_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msxml6.h
api_name:
-	IXMLHTTPRequest2Callback.OnRedirect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest2Callback::OnRedirect


## -description


Occurs when a client sends an HTTP request that the server redirects to a new URL.


## -parameters




### -param pXHR [in, optional]

The HTTP request object being redirected.


### -param pwszRedirectUrl [in]

The new URL for the HTTP request.


## -returns



Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>



## -remarks



If the request redirection is not permitted, you can call the Abort method on the pXHR object.

XMLHTTPRequest2 imposes a maximum of 100 re-directions on any request. Any re-directions above that limit generate an <a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a> event.
Applications have no access to the headers for re-directions.


 Once the final redirection has completed and the final URL has been reached, the application receives an <a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a> callback.





## -see-also




<a href="https://msdn.microsoft.com/B051D464-2328-44A2-A2BC-D0CDDCA79C64">Abort Method</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>



<a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError Event</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable Event</a>
 

 

