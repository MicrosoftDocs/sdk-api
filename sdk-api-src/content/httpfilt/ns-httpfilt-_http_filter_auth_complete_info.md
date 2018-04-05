---
UID: NS:httpfilt._HTTP_FILTER_AUTH_COMPLETE_INFO
title: "_HTTP_FILTER_AUTH_COMPLETE_INFO"
author: windows-driver-content
description: The Forefront TMG Web proxy includes a pointer to the HTTP_FILTER_AUTH_COMPLETE_INFO structure in the notification that it sends to Web filters after it has successfully completed authentication.
old-location: tmg\http_filter_auth_complete_info.htm
old-project: TMG
ms.assetid: 1e4010a3-60a8-4af0-b6c8-4889e65f4276
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PHTTP_FILTER_AUTH_COMPLETE_INFO, HTTP_FILTER_AUTH_COMPLETE_INFO, HTTP_FILTER_AUTH_COMPLETE_INFO structure [Forefront TMG], PHTTP_FILTER_AUTH_COMPLETE_INFO, PHTTP_FILTER_AUTH_COMPLETE_INFO structure pointer [Forefront TMG], _HTTP_FILTER_AUTH_COMPLETE_INFO, httpfilt/HTTP_FILTER_AUTH_COMPLETE_INFO, httpfilt/PHTTP_FILTER_AUTH_COMPLETE_INFO, tmg.http_filter_auth_complete_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: httpfilt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported,Forefront Threat Management Gateway (TMG) 2010
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 (64-bit only) [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: HTTP_FILTER_AUTH_COMPLETE_INFO, *PHTTP_FILTER_AUTH_COMPLETE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_AUTH_COMPLETE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_AUTH_COMPLETE_INFO structure


## -description


The Forefront TMG Web proxy includes a pointer to the <b>HTTP_FILTER_AUTH_COMPLETE_INFO</b> structure in the notification that it sends to Web filters after it has successfully completed authentication. If your filter should be notified for this event, it must register to receive SF_NOTIFY_AUTH_COMPLETE notifications. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.
<div class="alert"><b>Note</b>  When you are creating a Web filter for Forefront TMG, we recommend that you use <a href="https://msdn.microsoft.com/0619687d-a163-469f-a8f5-958414c83d8a">WPX_HTTP_FILTER_AUTH_COMPLETE_INFO</a> rather than <b>HTTP_FILTER_AUTH_COMPLETE_INFO</b>.</div><div> </div>

## -struct-fields




### -field GetHeader

Pointer to the <a href="https://msdn.microsoft.com/444bac76-4bf9-4ccc-bdf8-35cab14b1476">GetHeader</a> callback function, which can be used to retrieve a specified header or a portion of the request line in the incoming request. Header names include a trailing colon (:). Individual portions of the request line are specified by the special values "method", "URL", and "version". The special values are case-sensitive and must not include the trailing colon.


### -field SetHeader

Pointer to the <a href="https://msdn.microsoft.com/57bc61f9-1e3e-480f-bc96-58317dbbee36">SetHeader</a> callback function, which can be used to modify or delete the value of a header or to add a new header. Unlike the IIS function of the same name, this function cannot be used to modify the portions of the request line specified by the special values.


### -field AddHeader

Pointer to the <a href="https://msdn.microsoft.com/de595419-3311-4935-8399-0cde0915397a">AddHeader</a> callback function, which can be used to add an HTTP header to the request.


### -field GetUserToken

Pointer to the <a href="https://msdn.microsoft.com/0c17ee26-0052-49be-b432-09be038f1e9c">GetUserToken</a> function that returns a handle to the token of the user for whom impersonation will be performed.


### -field HttpStatus

Not used.


### -field fResetAuth

If set to <b>TRUE</b>, the authentication process will be reset, and no impersonation will be done.


### -field dwReserved

A <b>DWORD</b> reserved for later use.


## -remarks



This structure allows you to view the method, URL, version, or headers, or to modify the headers sent from the client.

The SF_NOTIFY_AUTH_COMPLETE notification is sent after the client's identity has been negotiated with the client, or when the client is anonymous. Because of the timing of this notification, the AUTH_USER server variable can be used to reliably obtain the identity of the user. Also, functionality is provided to retrieve a copy of the token that Forefront TMG will use to impersonate the client when processing the request.

All authentication scheme processes should result in either SF_NOTIFY_AUTH_COMPLETE, authentication, giving the filter a handle to a token of the user to be impersonated, or ACCESS_DENIED, when the user is not recognized by the system.

The SF_NOTIFY_AUTH_COMPLETE notification may be used for:

<ul>
<li>Accessing the user token of the user to be impersonated.</li>
<li>Actions that can be done in PREPROC_HEADERS, such as GET/ADD or SET request headers.</li>
<li>Resetting authentication.</li>
</ul>
<div class="alert"><b>Note</b>  If a filter needs to add Authorization headers after a request is authenticated and before the request is sent to the upstream proxy server or Web server, it must do so by parsing the request after the SF_NOTIFY_FORWARD_RAW_DATA notification, rather than after the SF_NOTIFY_AUTH_COMPLETE notification.
				<p class="note">This is because when the request is authenticated, Forefront TMG removes every Authorization header before sending the request on to the upstream proxy server or Web server. (In forward-proxy scenarios, it removes Proxy-Authorization headers. In reverse-proxy scenarios, it removes Authorization headers.) Therefore, even if the filter adds an Authorization header after receiving the SF_NOTIFY_AUTH_COMPLETE notification, it will be removed.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

