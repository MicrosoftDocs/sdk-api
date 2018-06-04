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
 

 

