---
UID: NS:httpfilt._HTTP_FILTER_ACCESS_DENIED
title: "_HTTP_FILTER_ACCESS_DENIED"
author: windows-driver-content
description: The Forefront TMG Web proxy includes a pointer to the HTTP_FILTER_ACCESS_DENIED structure in the notification that it sends to Web filters when a user is presented with an Access Denied error message.
old-location: tmg\http_filter_access_denied.htm
old-project: TMG
ms.assetid: e8309e1b-1717-48df-9c1e-6ed96785ca55
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PHTTP_FILTER_ACCESS_DENIED, HTTP_FILTER_ACCESS_DENIED, HTTP_FILTER_ACCESS_DENIED structure [Forefront TMG], PHTTP_FILTER_ACCESS_DENIED, PHTTP_FILTER_ACCESS_DENIED structure pointer [Forefront TMG], SF_DENIED_BY_CONFIG, SF_DENIED_FILTER, SF_DENIED_LOGON, SF_DENIED_RESOURCE, _HTTP_FILTER_ACCESS_DENIED, httpfilt/HTTP_FILTER_ACCESS_DENIED, httpfilt/PHTTP_FILTER_ACCESS_DENIED, tmg.http_filter_access_denied"
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
req.typenames: HTTP_FILTER_ACCESS_DENIED, *PHTTP_FILTER_ACCESS_DENIED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_ACCESS_DENIED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_ACCESS_DENIED structure


## -description


The Forefront TMG Web proxy includes a pointer to the <b>HTTP_FILTER_ACCESS_DENIED</b> structure in the notification that it sends to Web filters when a user is presented with an Access Denied error message. If your filter should be notified for this event, it must register to receive SF_NOTIFY_ACCESS_DENIED notifications. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.


## -struct-fields




### -field pszURL

A null-terminated string that specifies the URL that requested access to the resource.


### -field pszPhysicalPath

A null-terminated string that specifies the physical path of the resource that was requested.


### -field dwReason

A <b>DWORD</b> date type containing flags that indicate the reasons for the denial. It can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SF_DENIED_LOGON"></a><a id="sf_denied_logon"></a><dl>
<dt><b>SF_DENIED_LOGON</b></dt>
</dl>
</td>
<td width="60%">
The client could not be logged on.

</td>
</tr>
<tr>
<td width="40%"><a id="SF_DENIED_RESOURCE"></a><a id="sf_denied_resource"></a><dl>
<dt><b>SF_DENIED_RESOURCE</b></dt>
</dl>
</td>
<td width="60%">
The resource was denied by a Windows discretionary access control list (DACL).

</td>
</tr>
<tr>
<td width="40%"><a id="SF_DENIED_FILTER"></a><a id="sf_denied_filter"></a><dl>
<dt><b>SF_DENIED_FILTER</b></dt>
</dl>
</td>
<td width="60%">
A Web filter denied the request.

</td>
</tr>
<tr>
<td width="40%"><a id="SF_DENIED_BY_CONFIG"></a><a id="sf_denied_by_config"></a><dl>
<dt><b>SF_DENIED_BY_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
The server configuration denied the request. For example, disabling anonymous requests on the server would generate this filter notification when a user without credentials tried to make a request to the server.

</td>
</tr>
</table>
 


## -remarks



This structure indicates that access to the requested resource has been denied by the server. The structure is generated when there has been a logon failure.




## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

