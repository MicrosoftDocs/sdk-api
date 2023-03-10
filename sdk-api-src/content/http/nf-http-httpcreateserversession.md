---
UID: NF:http.HttpCreateServerSession
title: HttpCreateServerSession function (http.h)
description: Creates a server session for the specified version.
helpviewer_keywords: ["HttpCreateServerSession","HttpCreateServerSession function [HTTP]","http.httpcreateserversession","http/HttpCreateServerSession"]
old-location: http\httpcreateserversession.htm
tech.root: http
ms.assetid: 42c8be3a-eb1b-49ff-ade0-16e4500b0c44
ms.date: 12/05/2018
ms.keywords: HttpCreateServerSession, HttpCreateServerSession function [HTTP], http.httpcreateserversession, http/HttpCreateServerSession
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpCreateServerSession
 - http/HttpCreateServerSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpCreateServerSession
---

# HttpCreateServerSession function


## -description

The <b>HttpCreateServerSession</b> function creates a server session for the specified version.

## -parameters

### -param Version [in]

An HTTPAPI_VERSION structure that indicates the version of the server session. For  version 2.0, declare an instance of the structure and set it to the predefined value <b>HTTPAPI_VERSION_2</b> before passing it to <b>HttpCreateServerSession</b>.

The version must be 2.0; <b>HttpCreateServerSession</b> does not support  version 1.0 request queues.

### -param ServerSessionId [out]

A pointer to the variable that receives the ID of the server session.

### -param Reserved [in]

Reserved. Must be zero.

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

Server sessions own a set of URL Groups. They are top-level configuration containers for configuration information that applies to all of the URL Groups created under them. For more information about configuring a server session, see <a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>.

The HTTP Server API does not support asynchronous I/O for server sessions.

 When the server session is no longer required, or before the application terminates, application must delete the server session by calling <a href="/windows/desktop/api/http/nf-http-httpcloseserversession">HttpCloseServerSession</a>. When a server session is deleted all of the associated URL Groups are also automatically deleted.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseserversession">HttpCloseServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateserversession">HttpCreateServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>