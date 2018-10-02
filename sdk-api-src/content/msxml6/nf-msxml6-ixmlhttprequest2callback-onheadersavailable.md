---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnHeadersAvailable
title: IXMLHTTPRequest2Callback::OnHeadersAvailable
author: windows-sdk-content
description: Occurs after an HTTP request has been sent to the server and the server has responded with response headers.
old-location: ixhr2\ixmlhttprequest2callback_onheadersavailable.htm
tech.root: ixhr2
ms.assetid: EB6580C5-B200-4281-BF1F-FA5C3220689E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnHeadersAvailable method, IXMLHTTPRequest2Callback.OnHeadersAvailable, IXMLHTTPRequest2Callback::OnHeadersAvailable, OnHeadersAvailable, OnHeadersAvailable method [XMLHttpRequest2], OnHeadersAvailable method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onheadersavailable, msxml6/IXMLHTTPRequest2Callback::OnHeadersAvailable
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXMLHTTPRequest2Callback.OnHeadersAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXMLHTTPRequest2Callback::OnHeadersAvailable


## -description


Occurs after an HTTP request has been sent to the server and the server has  responded with response headers.


## -parameters




### -param pXHR [in, optional]

The initial HTTP request object that returns the headers.


### -param dwStatus [in]

The status code for the request.

<div class="alert"><b>Note</b>  Possible values for this parameter also include the <b>HTTP_STATUS_*</b> values defined by <b>winhttp.h</b> for  desktop apps.</div>
<div> </div>

### -param pwszStatus [in]

The status code for the request appearing in human-readable form as a null-terminated string.


## -returns



Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>



## -remarks



To view an individual response header, call the <a href="https://msdn.microsoft.com/5D68DAAA-D359-4FDF-8250-14A8D732FFFA">GetResponseHeader</a> method on the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> interface. To view all response headers, call the <a href="https://msdn.microsoft.com/6452812B-0E0F-4140-8E3C-25592A9C6C48">GetAllResponseHeaders</a> method. To cancel the request, call the Abort method On the pXHR object.




## -see-also




<a href="https://msdn.microsoft.com/6452812B-0E0F-4140-8E3C-25592A9C6C48">GetAllResponseHeaders Method</a>



<a href="https://msdn.microsoft.com/5D68DAAA-D359-4FDF-8250-14A8D732FFFA">GetResponseHeader Method</a>



<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a>
 

 

