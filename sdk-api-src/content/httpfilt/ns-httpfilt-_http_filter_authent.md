---
UID: NS:httpfilt._HTTP_FILTER_AUTHENT
title: "_HTTP_FILTER_AUTHENT"
author: windows-driver-content
description: The Forefront TMG Web proxy includes a pointer to the HTTP_FILTER_AUTHENT structure in the notification that it sends to Web filters when it is ready to authenticate a user.
old-location: tmg\http_filter_authent.htm
old-project: TMG
ms.assetid: 947b1449-96e6-4cf4-9403-eca09b2340bf
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PHTTP_FILTER_AUTHENT, HTTP_FILTER_AUTHENT, HTTP_FILTER_AUTHENT structure [Forefront TMG], PHTTP_FILTER_AUTHENT, PHTTP_FILTER_AUTHENT structure pointer [Forefront TMG], _HTTP_FILTER_AUTHENT, httpfilt/HTTP_FILTER_AUTHENT, httpfilt/PHTTP_FILTER_AUTHENT, tmg.http_filter_authent"
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
req.typenames: HTTP_FILTER_AUTHENT, *PHTTP_FILTER_AUTHENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Httpfilt.h
api_name:
-	HTTP_FILTER_AUTHENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_FILTER_AUTHENT structure


## -description


The Forefront TMG Web proxy includes a pointer to the <b>HTTP_FILTER_AUTHENT</b> structure in the notification that it sends to Web filters when it is ready to authenticate a user. If your filter should be notified for this event, it must register to receive SF_NOTIFY_AUTHENTICATION notifications. For more information about the types of event notifications that are sent to Web filters, see <a href="https://msdn.microsoft.com/288ec01e-1f1b-41ca-b433-d12053501979">Event Notifications</a>.
<div class="alert"><b>Note</b>  When you are creating a Web filter for Forefront TMG, we recommend that you use <a href="https://msdn.microsoft.com/286f049d-011f-4fff-9988-715029a4ddd0">WPX_FILTER_AUTHENT_EX</a> rather than <b>HTTP_FILTER_AUTHENT</b>.</div><div> </div>

## -struct-fields




### -field pszUser

Null-terminated string that specifies the user name for this request. An empty string indicates an anonymous user.


### -field cbUserBuff

The size of the buffer pointed to by <b>pszUser</b>. This is guaranteed to be at least SF_MAX_USERNAME.


### -field pszPassword

Null-terminated string that specifies the password for this request.


### -field cbPasswordBuff

The size of the buffer pointed to by <b>pszPassword</b>. This is guaranteed to be at least SF_MAX_PASSWORD.


## -remarks



When the server is about to authenticate the client, this structure is pointed to by the <i>pvNotification</i> parameter in the <a href="https://msdn.microsoft.com/15a44eb7-641b-4115-992e-6d08cb09be54">HttpFilterProc</a> function when the <i>notificationType</i> parameter is SF_NOTIFY_AUTHENTICATION. The <b>pszUser</b> and <b>pszPassword</b> members contain the information sent by the client. 

In the case of basic or RADIUS authentication, after exiting this notification, these values should represent a valid Windows user account and password. If another authentication method is used, the password value will not be available.




## -see-also




<a href="https://msdn.microsoft.com/f6100648-ba45-496f-a339-97defa274888">Notification Structures</a>
 

 

