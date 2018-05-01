---
UID: NF:http.HttpCloseUrlGroup
title: HttpCloseUrlGroup function
author: windows-driver-content
description: Closes the URL Group identified by the URL Group ID.
old-location: http\httpcloseurlgroup.htm
old-project: Http
ms.assetid: 8b8e4ec9-3d85-4d64-98dc-86e5fd093e93
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: HttpCloseUrlGroup, HttpCloseUrlGroup function [HTTP], http.httpcloseurlgroup, http/HttpCloseUrlGroup
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Httpapi.dll
api_name:
-	HttpCloseUrlGroup
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpCloseUrlGroup function


## -description


The <b>HttpCloseUrlGroup</b> function closes the URL Group identified by the URL Group ID. This call also removes all of the URLs that are associated with the URL Group.


## -parameters




### -param UrlGroupId [in]

The ID of the URL Group that is deleted.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The ID of the URL Group does not exist.

The application does not have permission to close the URL Group. Only the application that created the URL Group can close the group.

</td>
</tr>
</table>
 




## -remarks



Applications must call <b>HttpCloseUrlGroup</b> before calling <a href="https://msdn.microsoft.com/d1ceb491-c726-4aa0-b17e-f98f34279e32">HttpCloseServerSession</a> to close the all URL Groups associated with the server session.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>



<a href="https://msdn.microsoft.com/6f2b14bb-ecb9-4a63-9bef-e2ceaf09f97a">HttpCreateUrlGroup</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/9c5c1fec-f3b4-414f-a841-e360f5f4e4db">HttpRemoveUrlFromUrlGroup</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

