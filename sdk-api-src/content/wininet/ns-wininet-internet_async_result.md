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

# INTERNET_ASYNC_RESULT structure


## -description


Contains the result of a call to an asynchronous function. This structure is used with 
<a href="https://msdn.microsoft.com/a054fb71-66ab-46fd-be19-2237f05662bc">InternetStatusCallback</a>.


## -struct-fields




### -field dwResult

Result. This parameter can be an 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handle, unsigned long integer, or Boolean return code from an asynchronous function. 


### -field dwError

Error code, if 
<b>dwResult</b> indicates that the function failed. If the operation succeeded, this member usually contains ERROR_SUCCESS. 


## -remarks



The value of 
<b>dwResult</b> is determined by the value of  
<i>dwInternetStatus</i> in  the status callback function.
				


<table class="clsStd">
<tr>
<th>Value of 
<i>dwInternetStatus</i></th>
<th>Value of 
<b>dwResult</b></th>
</tr>
<tr>
<td>INTERNET_STATUS_HANDLE_CREATED</td>
<td>Pointer to the 
<a href="https://msdn.microsoft.com/8a9788ed-eb25-42cb-b912-8dffa3df1850">HINTERNET</a> handle</td>
</tr>
<tr>
<td>INTERNET_STATUS_REQUEST_COMPLETE</td>
<td>Boolean return code from the asynchronous function.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68"> Asynchronous Operation</a>
 

 

