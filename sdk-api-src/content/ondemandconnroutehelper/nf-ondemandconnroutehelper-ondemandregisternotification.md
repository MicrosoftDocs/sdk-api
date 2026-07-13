---
UID: NF:ondemandconnroutehelper.OnDemandRegisterNotification
title: OnDemandRegisterNotification function (ondemandconnroutehelper.h)
description: The OnDemandRegisterNotification function allows an application to register to be notified when the Route Requests cache is modified.
helpviewer_keywords: ["OnDemandRegisterNotification","OnDemandRegisterNotification function [Network Awareness]","nla.ondemandregisternotification","ondemandconnroutehelper/OnDemandRegisterNotification"]
old-location: nla\ondemandregisternotification.htm
tech.root: nla
ms.assetid: 1C9BB656-B1A7-49A6-97B9-414946BF9BE0
ms.date: 12/05/2018
ms.keywords: OnDemandRegisterNotification, OnDemandRegisterNotification function [Network Awareness], nla.ondemandregisternotification, ondemandconnroutehelper/OnDemandRegisterNotification
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
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OnDemandRegisterNotification
 - ondemandconnroutehelper/OnDemandRegisterNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OnDemandConnRouteHelper.dll
api_name:
 - OnDemandRegisterNotification
---

# OnDemandRegisterNotification function


## -description

The <b>OnDemandRegisterNotification</b> function allows an application to register to be notified when the Route Requests cache is modified. For example, this allows  the system to recycle cached connections when a Route Request is added or removed from the cache.

## -parameters

### -param callback [in]

A pointer to a function of type <b>ONDEMAND_NOTIFICATION_CALLBACK</b> to receive the notifications.

### -param callbackContext [in, optional]

A pointer to a memory location containing optional context to be passed to the callback.

### -param registrationHandle [out]

A pointer to a HANDLE to receive a handle to the registration in case of success.

## -returns

Returns S_OK on success.

## -remarks

The <b>ONDEMAND_NOTIFICATION_CALLBACK</b> function is defined as:


``` syntax
typedef void (WINAPI *ONDEMAND_NOTIFICATION_CALLBACK) (PVOID);
```


## -see-also

<a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-ondemandunregisternotification">OnDemandUnregisterNotification</a>
