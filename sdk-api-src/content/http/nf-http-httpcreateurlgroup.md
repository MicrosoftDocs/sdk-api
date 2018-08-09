---
UID: NF:http.HttpCreateUrlGroup
title: HttpCreateUrlGroup function
author: windows-sdk-content
description: Creates a URL Group under the specified server session.
old-location: http\httpcreateurlgroup.htm
old-project: http
ms.assetid: 6f2b14bb-ecb9-4a63-9bef-e2ceaf09f97a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HttpCreateUrlGroup, HttpCreateUrlGroup function [HTTP], http.httpcreateurlgroup, http/HttpCreateUrlGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpCreateUrlGroup
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpCreateUrlGroup function


## -description


The <b>HttpCreateUrlGroup</b> function creates a URL Group  under the specified  server session.


## -parameters




### -param ServerSessionId [in]

The identifier of the server session under which the URL Group is created.


### -param pUrlGroupId [out]

A pointer to the variable that receives the ID of the URL Group.


### -param Reserved [in]

Reserved. Must be zero.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ServerSessionId</i> parameter indicates  a non-existing Server Session.

The <i>pUrlGroupId</i> parameter is null.

The <i>Reserved</i> parameter is non-zero.

</td>
</tr>
</table>
 




## -remarks



URL Groups are configuration containers for a set of URLs. They are created under the server session and inherit the configuration settings of the server session. When a configuration parameter is set on the URL Group, it overrides the configuration set on the server session. For more information about the setting configurations for the URL Group, see <a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>.

After the URL group is created it must be associated with a request queue to receive requests. To associate the URL Group with a request queue, the application calls <a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a> with the <b>HttpServerBindingProperty</b> property. If this property is not set, matching requests for the URL Group are not delivered to a request queue and the  HTTP Server API generates a 503 response.

The URL Group association with a request queue is dynamic. The association with the servers session cannot be changed until either the server session or the URL Group is deleted. When a server session is deleted all of the associated URL Groups are also automatically closed. 

The URL Group is initially created as an empty group. URLs must be added to the group by calling <a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>.

Application may create multiple URL Groups for the following reasons:<ul>
<li>To set distinct configurations for different portions of URL name space on which it is listening.</li>
<li>To set separate request queues for different portions of URL name space on which it is listening.</li>
</ul>


Applications should combine URLs into groups as much  as possible; otherwise performance will degrade and increased memory consumption of the system will affect the scalability.

The HTTP Server API does not support asynchronous I/O on URL Groups.

When the URL group is no longer needed or before the application terminates it must delete the URL Group by calling <a href="https://msdn.microsoft.com/8b8e4ec9-3d85-4d64-98dc-86e5fd093e93">HttpCloseUrlGroup</a>.

The URL Group is created with the same version as the server session under which it is created.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>



<a href="https://msdn.microsoft.com/8b8e4ec9-3d85-4d64-98dc-86e5fd093e93">HttpCloseUrlGroup</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/9c5c1fec-f3b4-414f-a841-e360f5f4e4db">HttpRemoveUrlFromUrlGroup</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

