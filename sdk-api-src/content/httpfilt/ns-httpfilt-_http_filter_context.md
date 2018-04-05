---
UID: NS:httpfilt._HTTP_FILTER_CONTEXT
title: "_HTTP_FILTER_CONTEXT"
author: windows-driver-content
description: The HTTP_FILTER_CONTEXT structure is used for passing control and information associated with the current, active HTTP session in event notifications that are sent by the Forefront TMG Web proxy to Web filters by calling HttpFilterProc and HttpWPXFilterProc.
old-location: tmg\http_filter_context.htm
old-project: TMG
ms.assetid: 00b9f42c-46e1-4ef3-a7f3-73ac31cef2dd
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PHTTP_FILTER_CONTEXT, HTTP_FILTER_CONTEXT, HTTP_FILTER_CONTEXT structure [Forefront TMG], PHTTP_FILTER_CONTEXT, PHTTP_FILTER_CONTEXT structure pointer [Forefront TMG], _HTTP_FILTER_CONTEXT, httpfilt/HTTP_FILTER_CONTEXT, httpfilt/PHTTP_FILTER_CONTEXT, tmg.http_filter_context"
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
req.typenames: HTTP_FILTER_CONTEXT, *PHTTP_FILTER_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_CONTEXT structure


## -description


The <b>HTTP_FILTER_CONTEXT</b> structure is used for passing control and information associated with the current, active HTTP session in event notifications that are sent by the Forefront TMG Web proxy to Web filters by calling <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a> and <a href="https://msdn.microsoft.com/d0d25ed4-2cc7-4dd3-ba89-07e7370909b4">HttpWPXFilterProc</a>.


## -struct-fields




### -field cbSize

The size of this structure, in bytes.


### -field Revision

The revision level of this structure. 


### -field ServerContext

Reserved for server use.


### -field ulReserved

Reserved for server use.


### -field fIsSecurePort

A value of <b>TRUE</b> indicates that the event occurred over a secure port. A value of <b>FALSE</b> indicates that the event did not occur over a secure port.


### -field pFilterContext

Pointer to context information that the Web filter associates with the current, active HTTP session. It is initialized to <b>NULL</b> when the Web proxy creates the session, and it is set when the Web filter allocates memory to hold the context information. Any memory allocated for this context information can be safely freed during the SF_NOTIFY_END_OF_NET_SESSION notification.


### -field GetServerVariable

Pointer to the <a href="https://msdn.microsoft.com/7ca27b5b-f928-498e-acb8-dab813cf75c6">GetServerVariable</a> function that retrieves information about the server and the current connection. For some notifications, some variables may not be defined. For example, notifications that occur before PREPROC_HEADERS, such as the READ_RAW_DATA notification, may have undefined variables.


### -field AddResponseHeaders

Pointer to the <a href="https://msdn.microsoft.com/bdfd01cb-fa31-45a7-9ff8-38119948e266">AddResponseHeaders</a> function that adds a header to the HTTP response.


### -field WriteClient

Pointer to the <a href="https://msdn.microsoft.com/ee468491-2eeb-4786-92d5-e05b94ea439b">WriteClient</a> function that sends raw data back to the client.


### -field AllocMem

Pointer to the <a href="https://msdn.microsoft.com/41c826a0-5a23-4bac-9967-111ec447eca4">AllocMem</a> function used to allocate memory. Any memory allocated with this function will automatically be freed when the session ends.


### -field ServerSupportFunction

Pointer to the <a href="https://msdn.microsoft.com/9840c248-c527-431d-b8f1-2c5691abaf85">ServerSupportFunction</a> function used to extend the Web filter functions. Parameters are specific to the extensions.


## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

