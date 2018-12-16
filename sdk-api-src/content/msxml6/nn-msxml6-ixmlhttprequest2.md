---
UID: NN:msxml6.IXMLHTTPRequest2
title: IXMLHTTPRequest2
author: windows-sdk-content
description: Provides the methods and properties needed to configure and send HTTP requests and use callbacks to receive notifications during HTTP response processing. Note  This interface is supported on Windows Phone 8.1.  .
old-location: ixhr2\ixmlhttprequest2.htm
tech.root: ixhr2
ms.assetid: BBC11C4A-AECF-4D6D-8275-3E852E309908
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXMLHTTPRequest2, IXMLHTTPRequest2 interface [XMLHttpRequest2], IXMLHTTPRequest2 interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest2, msxml6/IXMLHTTPRequest2
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXMLHTTPRequest2 interface


## -description


Provides the methods and properties needed to configure and send HTTP requests and use  callbacks  to receive notifications  during HTTP response processing. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXMLHTTPRequest2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXMLHTTPRequest2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXMLHTTPRequest2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B051D464-2328-44A2-A2BC-D0CDDCA79C64">IXMLHTTPRequest2::Abort</a>
</td>
<td align="left" width="63%">
Cancels the current HTTP request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6452812B-0E0F-4140-8E3C-25592A9C6C48">IXMLHTTPRequest2::GetAllResponseHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the values of all the HTTP response headers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A2A9C54B-92A2-41EA-A741-797BA219BCDA">IXMLHTTPRequest2::GetCookie</a>
</td>
<td align="left" width="63%">
Gets a cookie associated with the specified URL from the HTTP cookie jar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D68DAAA-D359-4FDF-8250-14A8D732FFFA">IXMLHTTPRequest2::GetResponseHeader</a>
</td>
<td align="left" width="63%">
Retrieves the value of an HTTP header from the response headers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8723F24B-0739-44D6-8443-1A378B585F42">IXMLHTTPRequest2::Open</a>
</td>
<td align="left" width="63%">
Initializes an <b>IXMLHTTPRequest2</b> request and specifies the method, URL, and authentication information for the request.  After calling this method, you must call the <a href="https://msdn.microsoft.com/E46DB550-8346-41F2-9B35-4DFD9732B0D8">Send</a>  method to send the request and data, if any, to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E46DB550-8346-41F2-9B35-4DFD9732B0D8">IXMLHTTPRequest2::Send</a>
</td>
<td align="left" width="63%">
Sends an HTTP request to the server asynchronously. On success, methods on the <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> interface implemented by the app are called to process the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E150B7CA-A881-4CD5-896F-7E3B6770E105">IXMLHTTPRequest2::SetCookie</a>
</td>
<td align="left" width="63%">
Sets a cookie associated with the specified URL in the HTTP cookie jar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64341C82-85EC-402F-A875-85706DFD7B25">IXMLHTTPRequest2::SetCustomResponseStream</a>
</td>
<td align="left" width="63%">
Provides a custom stream to replace the standard stream for receiving an HTTP response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">IXMLHTTPRequest2::SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property on an outgoing HTTP request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FBEEB04C-7976-4017-B56C-17815FC01831">IXMLHTTPRequest2::SetRequestHeader</a>
</td>
<td align="left" width="63%">
Specifies the name of an HTTP header to be sent to the server along with the default request headers.

</td>
</tr>
</table> 


## -remarks



The <b>IXMLHTTPRequest2</b> interface is extended by the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface. The <b>IXMLHTTPRequest3</b> inherits all the methods and properties of the <b>IXMLHTTPRequest2</b> interface.

The <b>IXMLHTTPRequest2</b> interface configures and sends HTTP request operations and uses  callbacks  to receive notifications  during response processing. The <b>IXMLHTTPRequest2</b> allows applications to run in a Multi Threaded Apartment (MTA), a requirement for running under the Windows Runtime (WinRT).

The <b>IXMLHTTPRequest2</b> interface supports the following features:


<ul>
<li>Set properties on outgoing HTTP requests.</li>
<li>Set cookies in the HTTP cookie jar for use in outgoing HTTP requests.</li>
<li>Get cookies from the HTTP cookie jar.</li>
<li>Process incoming HTTP response data before the HTTP response has finished downloading.</li>
<li>Create custom streams to receive HTTP responses.</li>
</ul>


<b>IXMLHTTPRequest2</b> implements a callback model for event handling. Because <b>IXMLHTTPRequest2</b> methods allow only asynchronous method calls, to receive completion callbacks an application must pass a pointer to an <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> object when it calls the <a href="https://msdn.microsoft.com/8723F24B-0739-44D6-8443-1A378B585F42">IXMLHTTPRequest2::Open</a> method to create an HTTP request.




## -see-also




<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>



<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/CC7AED53-B2C5-4D83-B85D-CFF2F5BA7B35">Quickstart: Connecting using XML HTTP Request (IXHR2)</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=231482">Web authentication sample</a>
 

 

