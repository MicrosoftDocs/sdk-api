---
UID: NN:msxml6.IXMLHTTPRequest2Callback
title: IXMLHTTPRequest2Callback
author: windows-driver-content
description: Defines callbacks that notify an application with an outstanding IXMLHTTPRequest2 request of events that affect HTTP request and response processing. Note  This interface is supported on Windows Phone 8.1.  .
old-location: ixhr2\ixmlhttprequest2callback.htm
old-project: ixhr2
ms.assetid: AA4B3F4C-6E28-458B-BE25-6CCE8865FC71
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IXMLHTTPRequest2Callback, IXMLHTTPRequest2Callback interface [XMLHttpRequest2], IXMLHTTPRequest2Callback interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest2callback, msxml6/IXMLHTTPRequest2Callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IXMLHTTPRequest2Callback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IXMLHTTPRequest2Callback interface


## -description


Defines callbacks that notify an application with an outstanding <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>  request of events that affect HTTP request and response processing. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXMLHTTPRequest2Callback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXMLHTTPRequest2Callback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXMLHTTPRequest2Callback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/068C3288-A872-43FA-BF1F-D7A3CD2E2203">IXMLHTTPRequest2Callback::OnDataAvailable</a>
</td>
<td align="left" width="63%">
Occurs when a client receives part of the HTTP response data from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">IXMLHTTPRequest2Callback::OnError</a>
</td>
<td align="left" width="63%">
Occurs when an error is encountered or the request has been aborted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">IXMLHTTPRequest2Callback::OnHeadersAvailable</a>
</td>
<td align="left" width="63%">
Occurs after an HTTP request has been sent to the server and the server has  responded with response headers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8492FFD5-99C8-4545-B5FD-465CC01D0038">IXMLHTTPRequest2Callback::OnRedirect</a>
</td>
<td align="left" width="63%">
Occurs when a client sends an HTTP request that the server redirects to a new URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D1D4D4B-CC49-4A63-A0D5-B29D618E80DE">IXMLHTTPRequest2Callback::OnResponseReceived</a>
</td>
<td align="left" width="63%">
Occurs when a client has received a complete response from the server.

</td>
</tr>
</table> 


## -remarks



Methods on the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> interface are asynchronous, so applications must pass an <b>IXMLHTTPRequest2Callback</b> object as a parameter in calls to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> method on the <b>IXMLHTTPRequest2</b> interface to receive callback notifications. 

The <b>IXMLHTTPRequest2Callback</b> interface is extended by the <a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
 

 

