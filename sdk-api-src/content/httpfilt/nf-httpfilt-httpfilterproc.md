---
UID: NF:httpfilt.HttpFilterProc
title: HttpFilterProc function
author: windows-driver-content
description: The HttpFilterProc function is called by the Forefront TMG Web proxy whenever an event for which the filter has registered in the GetFilterVersion function occurs.
old-location: tmg\httpfilterproc.htm
old-project: TMG
ms.assetid: 15a44eb7-641b-4115-992e-6d08cb09be54
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: HttpFilterProc, HttpFilterProc callback function [Forefront TMG], httpfilt/HttpFilterProc, tmg.httpfilterproc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: HTTP_VERSION, *PHTTP_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Httpfilt.h
api_name:
-	HttpFilterProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HttpFilterProc function


## -description


The <b>HttpFilterProc</b> function is called by the Forefront TMG Web proxy whenever an event for which the filter has registered in the <a href="https://msdn.microsoft.com/9dcca0b7-e19e-4e8e-974f-fa70f1fd0b97">GetFilterVersion</a> function occurs. The Web proxy uses this function to pass information and control to the Web filter. This function must be implemented together with <b>GetFilterVersion</b>.

Information about notifications is provided in <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.

The declaration of <b>HttpFilterProc</b> is:


## -parameters




### -param pfc [in]

Pointer to the <a href="https://msdn.microsoft.com/00b9f42c-46e1-4ef3-a7f3-73ac31cef2dd">HTTP_FILTER_CONTEXT</a> data structure that is associated with the current, active HTTP session.


### -param NotificationType [in]

Flag that indicates the type of event notification that is being processed. For more information about the types of event notifications that are sent using this function, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.


### -param pvNotification [in]


						Pointer to the notification-specific structure that contains more information about the current context of the request. You should cast this pointer to a pointer to the relevant notification structure according to the notification type, which is listed in the following table. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.
						

<table>
<tr>
<th>Notification type</th>
<th>Notification structure</th>
</tr>
<tr>
<td>SF_NOTIFY_ACCESS_DENIED</td>
<td>
<a href="https://msdn.microsoft.com/e8309e1b-1717-48df-9c1e-6ed96785ca55">HTTP_FILTER_ACCESS_DENIED</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_AUTH_COMPLETE</td>
<td>
<a href="https://msdn.microsoft.com/1e4010a3-60a8-4af0-b6c8-4889e65f4276">HTTP_FILTER_AUTH_COMPLETE_INFO</a> or <a href="https://msdn.microsoft.com/0619687d-a163-469f-a8f5-958414c83d8a">WPX_HTTP_FILTER_AUTH_COMPLETE_INFO</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_AUTHENTICATION</td>
<td>
<a href="https://msdn.microsoft.com/947b1449-96e6-4cf4-9403-eca09b2340bf">HTTP_FILTER_AUTHENT</a> or <a href="https://msdn.microsoft.com/286f049d-011f-4fff-9988-715029a4ddd0">WPX_FILTER_AUTHENT_EX</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_LOG</td>
<td>
<a href="https://msdn.microsoft.com/c235937a-a7d4-48e9-b75c-5bbb09486041">HTTP_FILTER_LOG</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_PREPROC_HEADERS</td>
<td>
<a href="https://msdn.microsoft.com/2d12de6e-df42-4bde-882e-d23ed50cc9b8">HTTP_FILTER_PREPROC_HEADERS</a> or <a href="https://msdn.microsoft.com/babae2b8-4148-4443-8d36-16406cac0301">WPX_FILTER_PREPROC_HEADERS</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_READ_RAW_DATA</td>
<td>
<a href="https://msdn.microsoft.com/06fa039c-8007-4782-9cdc-197a52af7163">HTTP_FILTER_RAW_DATA</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_SEND_RAW_DATA</td>
<td>
<a href="https://msdn.microsoft.com/06fa039c-8007-4782-9cdc-197a52af7163">HTTP_FILTER_RAW_DATA</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_SEND_RESPONSE</td>
<td>
<a href="https://msdn.microsoft.com/cf0e79c9-a4b5-4617-93b9-49cdf401af7c">HTTP_FILTER_SEND_RESPONSE</a>
</td>
</tr>
<tr>
<td>SF_NOTIFY_URL_MAP</td>
<td>
<a href="https://msdn.microsoft.com/9cdd97f5-3361-4b5f-91fe-3996c37ff0f1">HTTP_FILTER_URL_MAP</a>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The SF_NOTIFY_END_OF_NET_SESSION and SF_NOTIFY_END_OF_REQUEST event notifications do not have corresponding structures. The pointer will contain a <b>NULL</b> value.</div>
<div> </div>

## -returns



Implementations of this function may return the following values to indicate how the event was handled.




## -remarks



This function usually serves as the dispatch for a Web filter. Separate functions are often created to serve as handlers for the individual notifications, especially if the handling code is complicated.

At a minimum, a Web filter must implement either <a href="https://msdn.microsoft.com/9dcca0b7-e19e-4e8e-974f-fa70f1fd0b97">GetFilterVersion</a> and <b>HttpFilterProc</b>, or <a href="https://msdn.microsoft.com/83f874bc-5d2c-4a47-89b9-55230fbcce9d">GetWPXFilterVersion</a> and <a href="https://msdn.microsoft.com/d0d25ed4-2cc7-4dd3-ba89-07e7370909b4">HttpWPXFilterProc</a> (or both pairs of functions).




## -see-also




<a href="https://msdn.microsoft.com/371c9784-7d7a-4020-8e49-a8b6a72f2b5c">Entry-Point Functions</a>
 

 

