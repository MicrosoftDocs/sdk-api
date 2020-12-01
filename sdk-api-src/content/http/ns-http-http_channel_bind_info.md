---
UID: NS:http._HTTP_CHANNEL_BIND_INFO
title: HTTP_CHANNEL_BIND_INFO (http.h)
description: HTTP_CHANNEL_BIND_INFO.
helpviewer_keywords: ["*PHTTP_CHANNEL_BIND_INFO","HTTP_CHANNEL_BIND_INFO","HTTP_CHANNEL_BIND_INFO structure [HTTP]","PHTTP_CHANNEL_BIND_INFO","PHTTP_CHANNEL_BIND_INFO structure pointer [HTTP]","http.http_channel_bind_info","http/HTTP_CHANNEL_BIND_INFO","http/PHTTP_CHANNEL_BIND_INFO"]
old-location: http\http_channel_bind_info.htm
tech.root: http
ms.assetid: 60428e66-9c08-418b-99e1-6824c638f2be
ms.date: 12/05/2018
ms.keywords: '*PHTTP_CHANNEL_BIND_INFO, HTTP_CHANNEL_BIND_INFO, HTTP_CHANNEL_BIND_INFO structure [HTTP], PHTTP_CHANNEL_BIND_INFO, PHTTP_CHANNEL_BIND_INFO structure pointer [HTTP], http.http_channel_bind_info, http/HTTP_CHANNEL_BIND_INFO, http/PHTTP_CHANNEL_BIND_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HTTP_CHANNEL_BIND_INFO, *PHTTP_CHANNEL_BIND_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_CHANNEL_BIND_INFO
 - http/_HTTP_CHANNEL_BIND_INFO
 - PHTTP_CHANNEL_BIND_INFO
 - http/PHTTP_CHANNEL_BIND_INFO
 - HTTP_CHANNEL_BIND_INFO
 - http/HTTP_CHANNEL_BIND_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_CHANNEL_BIND_INFO
---

# HTTP_CHANNEL_BIND_INFO structure


## -description

The <b>HTTP_CHANNEL_BIND_INFO</b>  structure is used to set or query channel bind authentication.

## -struct-fields

### -field Hardening

An <a href="/windows/desktop/api/http/ne-http-http_authentication_hardening_levels">HTTP_AUTHENTICATION_HARDENING_LEVELS</a> value indicating the hardening level  levels to be set or queried per server session or URL group.

### -field Flags

A bitwise OR combination of flags that determine the behavior of authentication.

The following values are supported.


<table>
<tr>
<td>Name</td>
<td>Value</td>
<td>Meaning</td>
</tr>
<tr>
<td>HTTP_CHANNEL_BIND_PROXY</td>
<td>0x1</td>
<td>The exact Channel Bind Token (CBT) match is bypassed. CBT is checked not to be equal to ‘unbound’. Service Principle Name (SPN) check is enabled. </td>
</tr>
<tr>
<td>HTTP_CHANNEL_BIND_PROXY_COHOSTING</td>
<td>Ox20</td>
<td>This flag is valid only if HTTP_CHANNEL_BIND_PROXY is also set. With the flag set, the CBT check (comparing with ‘unbound’) is skipped. The flag should be set if both secure channel traffic passed through proxy and traffic originally sent through insecure channel have to be authenticated. </td>
</tr>
<tr>
<td>HTTP_CHANNEL_BIND_NO_SERVICE_NAME_CHECK</td>
<td>0x2</td>
<td>SPN check always succeeds.</td>
</tr>
<tr>
<td>HTTP_CHANNEL_BIND_DOTLESS_SERVICE</td>
<td>0x4</td>
<td>Enables dotless service names.  Otherwise configuring CBT properties with dotless service names will fail. </td>
</tr>
<tr>
<td>HTTP_CHANNEL_BIND_SECURE_CHANNEL_TOKEN</td>
<td>0x8</td>
<td>Server session, URL group, or response is configured to retrieve secure channel endpoint binding for each request and pass it to user the mode application. When set, a pointer to a buffer with the secure channel endpoint binding is stored in an <a href="/windows/desktop/api/http/ns-http-http_request_channel_bind_status">HTTP_REQUEST_CHANNEL_BIND_STATUS</a> structure. </td>
</tr>
<tr>
<td>HTTP_CHANNEL_BIND_CLIENT_SERVICE</td>
<td>0x10</td>
<td>Server session, URL group, or response is configured to retrieve SPN for each request and pass it to the user mode application. The SPN is stored in the <b>ServiceName</b> field of the <a href="/windows/desktop/api/http/ns-http-http_request_channel_bind_status">HTTP_REQUEST_CHANNEL_BIND_STATUS</a> structure. The  type is always <b>HttpServiceBindingTypeW</b> (Unicode). 
</td>
</tr>
</table>

### -field ServiceNames

  Pointer to a buffer holding an array of 1 or more service names.  Each service name is represented by either an <a href="/windows/desktop/api/http/ns-http-http_service_binding_a">HTTP_SERVICE_BINDING_A</a> structure or an <a href="/windows/desktop/api/http/ns-http-http_service_binding_w">HTTP_SERVICE_BINDING_W</a> structure, dependent upon whether the name is ASCII or Unicode.  Regardless of which structure type is used, the array is cast into a pointer to an <a href="/windows/desktop/api/http/ns-http-http_service_binding_base">HTTP_SERVICE_BINDING_BASE</a> structure.

### -field NumberOfServiceNames

   
The number of names in <b>ServiceNames</b>.

## -remarks

<div class="alert"><b>Note</b>  <p class="note">This structure is used to set server session or URL group properties by passing it to <a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>  or <a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>.

<p class="note">The <b>HTTP_CHANNEL_BIND_INFO</b> structure is also returned when server session or URL group properties are queried

</div>
<div> </div>