---
UID: NF:http.HttpAddUrlToUrlGroup
title: HttpAddUrlToUrlGroup function
author: windows-sdk-content
description: Adds the specified URL to the URL Group identified by the URL Group ID.
old-location: http\httpaddurltourlgroup.htm
old-project: http
ms.assetid: e6bf68aa-d6a5-4079-b689-49cfc2303ba5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HttpAddUrlToUrlGroup, HttpAddUrlToUrlGroup function [HTTP], http.httpaddurltourlgroup, http/HttpAddUrlToUrlGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: http.h
req.include-header: 
req.redist: 
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
 - HttpAddUrlToUrlGroup
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpAddUrlToUrlGroup function


## -description


The <b>HttpAddUrlToUrlGroup</b> function adds the specified URL to  the URL Group identified by the URL Group ID.

 This function replaces the HTTP version 1.0 <a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a> function.


## -parameters




### -param UrlGroupId [in]

The group ID for the URL group to which requests for the specified URL are routed. The URL group is created by the <a href="https://msdn.microsoft.com/6f2b14bb-ecb9-4a63-9bef-e2ceaf09f97a">HttpCreateUrlGroup</a> function.


### -param pFullyQualifiedUrl [in]

A pointer to a Unicode string that contains a properly formed <a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix String</a> that identifies the URL to be registered.


### -param OPTIONAL

TBD


### -param Reserved [in]

Reserved. Must be zero.


#### - UrlContext [in, optional]

The context that is associated with the URL registered in this call. The URL context is returned in the <a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure with every request received on the URL specified in the <i>pFullyQualifiedUrl</i> parameter.


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
The <i>UrlGroupId</i> does not exist.

 The <i>Reserved</i> parameter is not zero.

The application does not have permission to add URLs to the Group. Only the application that created the URL Group can add URLs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process does not have permission to register the URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified URL conflicts with an existing registration.

</td>
</tr>
</table>
 




## -remarks



The HTTP Server API supports existing applications using version 1.0 URL registrations, however, new development with the HTTP Server API should use <b>HttpAddUrlToUrlGroup</b>; <a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a> should not be used.

An application can add multiple URLs to a URL group using repeated calls to <b>HttpAddUrlToUrlGroup</b>. Requests that match the specified  URL are routed to the request queue associated with the URL group. For more information about how the HTTP Server API matches request URLs to registered URLs, see <a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/76b228a0-6792-4184-bf0e-8638f3ab6b98">HttpAddUrl</a>



<a href="https://msdn.microsoft.com/8b8e4ec9-3d85-4d64-98dc-86e5fd093e93">HttpCloseUrlGroup</a>



<a href="https://msdn.microsoft.com/6f2b14bb-ecb9-4a63-9bef-e2ceaf09f97a">HttpCreateUrlGroup</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/9c5c1fec-f3b4-414f-a841-e360f5f4e4db">HttpRemoveUrlFromUrlGroup</a>



<a href="https://msdn.microsoft.com/e0826a25-1c50-4757-9355-69eb4946e8dd">HttpSetUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix Strings</a>
 

 

