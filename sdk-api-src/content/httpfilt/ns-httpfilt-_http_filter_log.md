---
UID: NS:httpfilt._HTTP_FILTER_LOG
title: "_HTTP_FILTER_LOG"
author: windows-driver-content
description: The Forefront TMG Web proxy includes a pointer to the HTTP_FILTER_LOG structure in the notification that it sends to Web filters when it is ready to write information to a log file.
old-location: tmg\http_filter_log.htm
old-project: TMG
ms.assetid: c235937a-a7d4-48e9-b75c-5bbb09486041
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PHTTP_FILTER_LOG, HTTP_FILTER_LOG, HTTP_FILTER_LOG structure [Forefront TMG], PHTTP_FILTER_LOG, PHTTP_FILTER_LOG structure pointer [Forefront TMG], _HTTP_FILTER_LOG, httpfilt/HTTP_FILTER_LOG, httpfilt/PHTTP_FILTER_LOG, tmg.http_filter_log"
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
req.typenames: HTTP_FILTER_LOG, *PHTTP_FILTER_LOG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_LOG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_LOG structure


## -description


The Forefront TMG Web proxy includes a pointer to the <b>HTTP_FILTER_LOG</b> structure in the notification that it sends to Web filters when it is ready to write information to a log file. If your filter should be notified for this event, it must register to receive SF_NOTIFY_LOG notifications. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.


## -struct-fields




### -field pszClientHostName

The client's host name or IP address.


### -field pszClientUserName

Null-terminated string that specifies the client's user name if authenticated, or "anonymous" otherwise.


### -field pszServerName

Null-terminated string that specifies the name of the server to which the client is connected.


### -field pszOperation

Null-terminated string that specifies the HTTP method.


### -field pszTarget

Null-terminated string that specifies the target of the HTTP command.


### -field pszParameters

Null-terminated string that specifies the parameters passed to the HTTP command. This member is used to store the information that is to written in the Filter Information field of a Web proxy log entry.


### -field dwHttpStatus

The HTTP return status.


### -field dwWin32Status

The Windows error code.


### -field dwBytesSent

The number of bytes sent from the server to the client.


### -field dwBytesRecvd

The number of bytes received by the server from the client.


### -field msTimeForProcessing

The time, in milliseconds, required to process the client request.


## -remarks



When the Web proxy is about to log information to the Web proxy log, it sends a notification by calling the <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a> entry-point function of each Web filter that is registered to receive SF_NOTIFY_LOG event notifications. The <i>pvNotification</i> parameter contains a pointer to an <b>HTTP_FILTER_LOG</b> structure, and the <i>notificationType</i> parameter is set to SF_NOTIFY_LOG.

The strings cannot be changed, but the string pointers can be replaced. If string pointers are changed, the memory they point to must remain valid until the next filter notification. The <a href="https://msdn.microsoft.com/41c826a0-5a23-4bac-9967-111ec447eca4">AllocMem</a> callback function in the HTTP_FILTER_CONTEXT structure can be used to ensure this.

The strings specified in the <b>pszClientHostName</b>,  <b>pszClientUserName</b>,  <b>pszServerName</b>,  <b>pszOperation</b>,  <b>pszTarget</b>,  and <b>pszParameters</b>  members are formatted with UCS Transformation Format 8 (UTF-8) encoding.

For more information about how a Web filter can write information to the Web proxy log, see <a href="https://msdn.microsoft.com/2bd8de1e-edd3-4edb-a067-3501cb9dec54">Adding Information to the Web Proxy Log</a>.




## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

