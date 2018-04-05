---
UID: NS:httpfilt._HTTP_FILTER_RAW_DATA
title: "_HTTP_FILTER_RAW_DATA"
author: windows-driver-content
description: The Forefront TMG Web proxy includes a pointer to the HTTP_FILTER_RAW_DATA structure in the notification that it sends to Web filters when it reads or is about to send raw data.
old-location: tmg\http_filter_raw_data.htm
old-project: TMG
ms.assetid: 06fa039c-8007-4782-9cdc-197a52af7163
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PHTTP_FILTER_RAW_DATA, HTTP_FILTER_RAW_DATA, HTTP_FILTER_RAW_DATA structure [Forefront TMG], PHTTP_FILTER_RAW_DATA, PHTTP_FILTER_RAW_DATA structure pointer [Forefront TMG], _HTTP_FILTER_RAW_DATA, httpfilt/HTTP_FILTER_RAW_DATA, httpfilt/PHTTP_FILTER_RAW_DATA, tmg.http_filter_raw_data"
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
req.typenames: HTTP_FILTER_RAW_DATA, *PHTTP_FILTER_RAW_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_RAW_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_RAW_DATA structure


## -description


The Forefront TMG Web proxy includes a pointer to the <b>HTTP_FILTER_RAW_DATA</b> structure in the notification that it sends to Web filters when it reads or is about to send raw data. If your filter should be notified for events involving reading or sending raw data, it must register to receive one or more of these notifications:
<ul>
<li>SF_NOTIFY_READ_RAW_DATA</li>
<li>SF_NOTIFY_SEND_RAW_DATA</li>
<li>SF_NOTIFY_FORWARD_RAW_DATA</li>
<li>SF_NOTIFY_RECEIVE_RESPONSE_RAW_DATA</li>
</ul>For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.


## -struct-fields




### -field pvInData

Pointer to the data buffer.


### -field cbInData

The amount of data, in bytes, in the buffer pointed to by <b>pvInData</b>.


### -field cbInBuffer

The size, in bytes, of the buffer pointed to by <b>pvInData</b>.


### -field dwReserved

Reserved for future use.


## -remarks



When the Web proxy sends an SF_NOTIFY_READ_RAW_DATA or SF_NOTIFY_SEND_RAW_DATA notification, this structure is pointed to by the <i>pvNotification</i> parameter in the <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a> entry-point function.  When the Web proxy sends an SF_NOTIFY_FORWARD_RAW_DATA or SF_NOTIFY_RECEIVE_RESPONSE_RAW_DATA notification, this structure is pointed to by the <i>pvNotification</i> parameter in the <a href="https://msdn.microsoft.com/d0d25ed4-2cc7-4dd3-ba89-07e7370909b4">HttpWPXFilterProc</a> entry-point function. Web filters that modify the raw data being sent or received can replace the <b>pvInData</b> pointer. (If the pointer is replaced, <b>cbInData</b> and <b>cbInBuffer</b> must also be appropriately updated.) The new buffer memory must remain valid until the end of the request. The new buffer memory can remain valid by using <a href="https://msdn.microsoft.com/41c826a0-5a23-4bac-9967-111ec447eca4">AllocMem</a> or <a href="https://msdn.microsoft.com/3706e15a-eecd-4ad3-a1c7-bf90d7a849eb">AllocMemoryPerRequest</a>, or by using a buffer owned by the filter. In addition, the filter must not attempt to free or otherwise deallocate the old <b>pvInData</b> pointer. Only the owner of the memory block can free the buffer.

If a filter accumulates a response in an SF_NOTIFY_RECEIVE_RESPONSE_RAW_DATA notification without releasing it to the next filter, the filter may not release the data until it receives an SF_NOTIFY_END_OF_REQUEST notification, which indicates that the server closed the connection. At this point, the filter will typically call <a href="https://msdn.microsoft.com/ee468491-2eeb-4786-92d5-e05b94ea439b">WriteClient</a> with the accumulated data. However, this will prevent other server-side filters from obtaining the raw response data, and those filters will be skipped. We recommend not accumulating the body of a response without releasing it to the next filter. If you must do so, accumulate the data in an SF_NOTIFY_SEND_RAW_DATA notification rather than an SF_NOTIFY_RECEIVE_RESPONSE_RAW_DATA notification.

<div class="alert"><b>Warning</b>  We do not recommend that filters modify the raw data in place. The memory segment may be read-only or the data may be cached directly by an ISAPI extension.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

