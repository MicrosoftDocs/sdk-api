---
UID: NF:http.HttpCloseServerSession
title: HttpCloseServerSession function (http.h)
description: Deletes the server session identified by the server session ID.
helpviewer_keywords: ["HttpCloseServerSession","HttpCloseServerSession function [HTTP]","http.httpcloseserversession","http/HttpCloseServerSession"]
old-location: http\httpcloseserversession.htm
tech.root: http
ms.assetid: d1ceb491-c726-4aa0-b17e-f98f34279e32
ms.date: 12/05/2018
ms.keywords: HttpCloseServerSession, HttpCloseServerSession function [HTTP], http.httpcloseserversession, http/HttpCloseServerSession
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
 - HttpCloseServerSession
 - http/HttpCloseServerSession
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
 - HttpCloseServerSession
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

Applications must call <a href="/windows/desktop/api/http/nf-http-httpcloseurlgroup">HttpCloseUrlGroup</a> before calling <b>HttpCloseServerSession</b> to close the all the URL Groups associated with the server session.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseserversession">HttpCloseServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateserversession">HttpCreateServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>