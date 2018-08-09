---
UID: NF:http.HttpCloseServerSession
title: HttpCloseServerSession function
author: windows-sdk-content
description: Deletes the server session identified by the server session ID.
old-location: http\httpcloseserversession.htm
old-project: http
ms.assetid: d1ceb491-c726-4aa0-b17e-f98f34279e32
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HttpCloseServerSession, HttpCloseServerSession function [HTTP], http.httpcloseserversession, http/HttpCloseServerSession
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
 - HttpCloseServerSession
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpCloseServerSession function


## -description


The <b>HttpCloseServerSession</b> function deletes the server session identified by the server session ID. All remaining URL Groups associated with the server session will also be closed.


## -parameters




### -param ServerSessionId [in]

The ID of the server session that is closed.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>

If the function fails, it can return one of the following error codes.

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
The Server Session does not exist.

The application does not have permission to close the server session. Only the application that created the server session can close the session.

</td>
</tr>
</table>
 




## -remarks



Applications must call <a href="https://msdn.microsoft.com/8b8e4ec9-3d85-4d64-98dc-86e5fd093e93">HttpCloseUrlGroup</a> before calling <b>HttpCloseServerSession</b> to close the all the URL Groups associated with the server session.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/d1ceb491-c726-4aa0-b17e-f98f34279e32">HttpCloseServerSession</a>



<a href="https://msdn.microsoft.com/42c8be3a-eb1b-49ff-ade0-16e4500b0c44">HttpCreateServerSession</a>



<a href="https://msdn.microsoft.com/653b286b-dc86-4896-8f03-1628b7178680">HttpQueryServerSessionProperty</a>



<a href="https://msdn.microsoft.com/d655832c-68a1-42d1-ac91-964884bf2dac">HttpSetServerSessionProperty</a>
 

 

