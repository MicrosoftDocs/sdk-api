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

# HttpCreateServerSession function


## -description


The <b>HttpCreateServerSession</b> function creates a server session for the specified version.


## -parameters




### -param Version [in]

An HTTPAPI_VERSION structure that indicates the version of the server session. For  version 2.0, declare an instance of the structure and set it to the predefined value <b>HTTPAPI_VERSION_2</b> before passing it to <b>HttpCreateServerSession</b>.

The version must be 2.0; <b>HttpCreateServerSession</b> does not support  version 1.0 request queues.


### -param ServerSessionId

TBD


### -param Reserved [in]

Reserved. Must be zero.


#### - pServerSessionId [out]

A pointer to the variable that receives the ID of the server session.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The version passed is invalid or unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pServerSessionId</i> parameter is null or the  <i>Reserved</i> is non zero.

</td>
</tr>
</table>
 




## -remarks



Server sessions own a set of URL Groups. They are top-level configuration containers for configuration information that applies to all of the URL Groups created under them. For more information about configuring a server session, see <a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>.

The HTTP Server API does not support asynchronous I/O for server sessions.

 When the server session is no longer required, or before the application terminates, application must delete the server session by calling <a href="https://msdn.microsoft.com/d1ceb491-c726-4aa0-b17e-f98f34279e32">HttpCloseServerSession</a>. When a server session is deleted all of the associated URL Groups are also automatically deleted.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/d1ceb491-c726-4aa0-b17e-f98f34279e32">HttpCloseServerSession</a>



<a href="https://msdn.microsoft.com/42c8be3a-eb1b-49ff-ade0-16e4500b0c44">HttpCreateServerSession</a>



<a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>



<a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>
 

 

