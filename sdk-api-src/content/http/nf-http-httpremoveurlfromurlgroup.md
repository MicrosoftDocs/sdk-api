---
UID: NF:http.HttpRemoveUrlFromUrlGroup
title: HttpRemoveUrlFromUrlGroup function (http.h)
author: windows-sdk-content
description: Removes the specified URL from the group identified by the URL Group ID.
old-location: http\httpremoveurlfromurlgroup.htm
tech.root: http
ms.assetid: 9c5c1fec-f3b4-414f-a841-e360f5f4e4db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HTTP_URL_FLAG_REMOVE_ALL, HttpRemoveUrlFromUrlGroup, HttpRemoveUrlFromUrlGroup function [HTTP], http.httpremoveurlfromurlgroup, http/HttpRemoveUrlFromUrlGroup
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpRemoveUrlFromUrlGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HttpRemoveUrlFromUrlGroup function


## -description


The <b>HttpRemoveUrlFromUrlGroup</b> function removes the specified URL from  the group identified by the URL Group ID. This function removes one, or all, of the URLs from the group. 

This function replaces the HTTP version 1.0 <a href="https://msdn.microsoft.com/21740d08-c280-44c1-8efb-1d21b4006039">HttpRemoveUrl</a> function.


## -parameters




### -param UrlGroupId [in]

The ID of the URL group from which the URL specified in <i>pFullyQualifiedUrl</i> is removed.


### -param pFullyQualifiedUrl [in]

A pointer to a Unicode string that contains a properly formed <a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix String</a> that identifies the URL to be removed.

When <b>HTTP_URL_FLAG_REMOVE_ALL</b> is passed in the <i>Flags</i> parameter, all of the existing URL registrations for the URL Group identified in <i>UrlGroupId</i> are removed from the group. In this case, <i>pFullyQualifiedUrl</i> must be <b>NULL</b>.


### -param Flags [in]

The URL flags qualifying the URL that is removed. This  can be one of the following flags:

<table>
<tr>
<th>URL Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_URL_FLAG_REMOVE_ALL"></a><a id="http_url_flag_remove_all"></a><dl>
<dt><b>HTTP_URL_FLAG_REMOVE_ALL</b></dt>
</dl>
</td>
<td width="60%">
Removes all of the URLs currently registered with the URL Group.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns NO_ERROR.

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
The URL Group does not exist.

The Flags parameter contains an invalid combination of flags.

The HTTP_URL_FLAG_REMOVE_ALL flag was set and the <i>pFullyQualifiedUrl</i> parameter was not set to <b>NULL</b>.

The application does not have permission to remove URLs from the Group. Only the application that created the URL Group can remove URLs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process does not have permission to deregister the URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified URL is not registered with the URL Group.

</td>
</tr>
</table>
 




## -remarks



The HTTP Server API supports existing applications using the version 1.0 URL registrations, however, new development with the HTTP Server API should use <b>HttpRemoveUrlFromUrlGroup</b>; do not use <a href="https://msdn.microsoft.com/21740d08-c280-44c1-8efb-1d21b4006039">HttpRemoveUrl</a>.

Applications should remove the URL added to the group by <a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>, when the URL is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>



<a href="https://msdn.microsoft.com/8b8e4ec9-3d85-4d64-98dc-86e5fd093e93">HttpCloseUrlGroup</a>



<a href="https://msdn.microsoft.com/6f2b14bb-ecb9-4a63-9bef-e2ceaf09f97a">HttpCreateUrlGroup</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/21740d08-c280-44c1-8efb-1d21b4006039">HttpRemoveUrl</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>
 

 

