---
UID: NF:ondemandconnroutehelper.OnDemandRegisterNotification
title: OnDemandRegisterNotification function
author: windows-sdk-content
description: The OnDemandRegisterNotification function allows an application to register to be notified when the Route Requests cache is modified.
old-location: nla\ondemandregisternotification.htm
old-project: NLA
ms.assetid: 1C9BB656-B1A7-49A6-97B9-414946BF9BE0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: OnDemandRegisterNotification, OnDemandRegisterNotification function [Network Awareness], nla.ondemandregisternotification, ondemandconnroutehelper/OnDemandRegisterNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ondemandconnroutehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: OLEVERB, *LPOLEVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OnDemandConnRouteHelper.dll
api_name:
-	OnDemandRegisterNotification
product: Windows
targetos: Windows
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OnDemandRegisterNotification function


## -description


The <b>OnDemandRegisterNotification</b> function allows an application to register to be notified when the Route Requests cache is modified. For example, this allows  the system to recycle cached connections when a Route Request is added or removed from the cache.


## -parameters




### -param callback

TBD


### -param callbackContext

TBD


### -param registrationHandle

TBD




#### - funcCallback [in]

A pointer to a function of type O<b>ONDEMAND_NOTIFICATION_CALLBACK</b> to receive the notifications.


#### - pCallbackContext [in, optional]

A pointer to a memory location containing optional context to be passed to the callback.


#### - pRegistrationHandle [out]

A pointer to a HANDLE to receive a handle to the registration in case of success.


## -returns



Returns S_OK on success.




## -remarks



The <b>ONDEMAND_NOTIFICATION_CALLBACK</b> function is defined as:

<pre class="syntax" xml:space="preserve"><code>typedef void (WINAPI *ONDEMAND_NOTIFICATION_CALLBACK) (PVOID);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/A7FA6035-D089-4A65-8F4E-F8722C147B0F">OnDemandUnregisterNotification</a>
 

 

