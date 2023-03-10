---
UID: NF:http.HttpCloseUrlGroup
title: HttpCloseUrlGroup function (http.h)
description: Closes the URL Group identified by the URL Group ID.
helpviewer_keywords: ["HttpCloseUrlGroup","HttpCloseUrlGroup function [HTTP]","http.httpcloseurlgroup","http/HttpCloseUrlGroup"]
old-location: http\httpcloseurlgroup.htm
tech.root: http
ms.assetid: 8b8e4ec9-3d85-4d64-98dc-86e5fd093e93
ms.date: 12/05/2018
ms.keywords: HttpCloseUrlGroup, HttpCloseUrlGroup function [HTTP], http.httpcloseurlgroup, http/HttpCloseUrlGroup
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
 - HttpCloseUrlGroup
 - http/HttpCloseUrlGroup
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
 - HttpCloseUrlGroup
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

Applications must call <b>HttpCloseUrlGroup</b> before calling <a href="/windows/desktop/api/http/nf-http-httpcloseserversession">HttpCloseServerSession</a> to close the all URL Groups associated with the server session.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurlfromurlgroup">HttpRemoveUrlFromUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>