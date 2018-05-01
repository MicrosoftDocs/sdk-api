---
UID: NS:httpfilt._HTTP_FILTER_PREPROC_HEADERS
title: "_HTTP_FILTER_PREPROC_HEADERS"
author: windows-driver-content
description: The Forefront TMG Web proxy includes a pointer to the HTTP_FILTER_PREPROC_HEADERS structure in the notification that it sends to Web filters when it preprocesses headers in a request.
old-location: tmg\http_filter_preproc_headers.htm
old-project: TMG
ms.assetid: 2d12de6e-df42-4bde-882e-d23ed50cc9b8
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PHTTP_FILTER_PREPROC_HEADERS, *PHTTP_FILTER_SEND_RESPONSE, HTTP_FILTER_PREPROC_HEADERS, HTTP_FILTER_PREPROC_HEADERS structure [Forefront TMG], HTTP_FILTER_SEND_RESPONSE, PHTTP_FILTER_PREPROC_HEADERS, PHTTP_FILTER_PREPROC_HEADERS structure pointer [Forefront TMG], _HTTP_FILTER_PREPROC_HEADERS, httpfilt/HTTP_FILTER_PREPROC_HEADERS, httpfilt/PHTTP_FILTER_PREPROC_HEADERS, tmg.http_filter_preproc_headers"
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
req.typenames: HTTP_FILTER_PREPROC_HEADERS, *PHTTP_FILTER_PREPROC_HEADERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_PREPROC_HEADERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_PREPROC_HEADERS structure


## -description


The Forefront TMG Web proxy includes a pointer to the <b>HTTP_FILTER_PREPROC_HEADERS</b> structure in the notification that it sends to Web filters when it preprocesses headers in a request. If your filter should be notified for this event, it must register to receive SF_NOTIFY_PREPROC_HEADERS event notifications. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.
<div class="alert"><b>Note</b>  When you are creating a Web filter for Forefront TMG, we recommend that you use <a href="https://msdn.microsoft.com/babae2b8-4148-4443-8d36-16406cac0301">WPX_FILTER_PREPROC_HEADERS</a> rather than <b>HTTP_FILTER_PREPROC_HEADERS</b>.</div><div> </div>

## -struct-fields




### -field GetHeader

Pointer to the <a href="https://msdn.microsoft.com/444bac76-4bf9-4ccc-bdf8-35cab14b1476">GetHeader</a> callback function, which can be used to retrieve a specified header or a portion of the request line in the incoming request. Header names include a trailing colon (:). Individual portions of the request line are specified by the special values "body", "method", "URL", and "version". The special values are case-sensitive and must not include the trailing colon.


### -field SetHeader

Pointer to the <a href="https://msdn.microsoft.com/57bc61f9-1e3e-480f-bc96-58317dbbee36">SetHeader</a> callback function, which can be used to modify or delete the value of a header or to modify a portion included in the request line specified by a special value.


### -field AddHeader

Pointer to the <a href="https://msdn.microsoft.com/de595419-3311-4935-8399-0cde0915397a">AddHeader</a> callback function, which can be used to add an HTTP header to the request.


### -field HttpStatus

Not used.


### -field dwReserved

A <b>DWORD</b> reserved for later use.


## -remarks



When the Web proxy is about to process the client headers, it sends a notification by calling the <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a> entry-point function of each Web filter that is registered to receive SF_NOTIFY_PREPROC_HEADERS event notifications. The <i>pvNotification</i> parameter contains a pointer to an <b>HTTP_FILTER_PREPROC_HEADERS</b> structure, and the <i>notificationType</i> parameter is set to SF_NOTIFY_PREPROC_HEADERS.




## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

