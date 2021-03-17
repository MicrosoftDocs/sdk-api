---
UID: NF:ondemandconnroutehelper.OnDemandUnRegisterNotification
title: OnDemandUnRegisterNotification function (ondemandconnroutehelper.h)
description: The OnDemandUnregisterNotification function allows an application to unregister for notifications and clean up resources.
helpviewer_keywords: ["OnDemandUnRegisterNotification","OnDemandUnregisterNotification","OnDemandUnregisterNotification function [Network Awareness]","nla.ondemandunregisternotification","ondemandconnroutehelper/OnDemandUnregisterNotification"]
old-location: nla\ondemandunregisternotification.htm
tech.root: nla
ms.assetid: A7FA6035-D089-4A65-8F4E-F8722C147B0F
ms.date: 12/05/2018
ms.keywords: OnDemandUnRegisterNotification, OnDemandUnregisterNotification, OnDemandUnregisterNotification function [Network Awareness], nla.ondemandunregisternotification, ondemandconnroutehelper/OnDemandUnregisterNotification
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
 - OnDemandUnRegisterNotification
 - ondemandconnroutehelper/OnDemandUnRegisterNotification
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
 - OnDemandUnregisterNotification
---

# OnDemandUnRegisterNotification function


## -description

The <b>OnDemandUnregisterNotification</b> function allows an application to unregister for notifications and clean up resources.

## -parameters

### -param registrationHandle [in]

A HANDLE obtained from a successful <a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-ondemandregisternotification">OnDemandRegisterNotification</a>  call.

## -returns

Returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-ondemandregisternotification">OnDemandRegisterNotification</a>