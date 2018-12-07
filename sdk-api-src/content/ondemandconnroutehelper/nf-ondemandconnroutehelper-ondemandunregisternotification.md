---
UID: NF:ondemandconnroutehelper.OnDemandUnRegisterNotification
title: OnDemandUnRegisterNotification function
author: windows-sdk-content
description: The OnDemandUnregisterNotification function allows an application to unregister for notifications and clean up resources.
old-location: nla\ondemandunregisternotification.htm
tech.root: nla
ms.assetid: A7FA6035-D089-4A65-8F4E-F8722C147B0F
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: OnDemandUnRegisterNotification, OnDemandUnregisterNotification, OnDemandUnregisterNotification function [Network Awareness], nla.ondemandunregisternotification, ondemandconnroutehelper/OnDemandUnregisterNotification
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OnDemandConnRouteHelper.dll
api_name:
 - OnDemandUnregisterNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OnDemandUnRegisterNotification function


## -description


The <b>OnDemandUnregisterNotification</b> function allows an application to unregister for notifications and clean up resources.


## -parameters




### -param registrationHandle [in]

A HANDLE obtained from a successful <a href="https://msdn.microsoft.com/1C9BB656-B1A7-49A6-97B9-414946BF9BE0">OnDemandRegisterNotification</a>  call.


## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/1C9BB656-B1A7-49A6-97B9-414946BF9BE0">OnDemandRegisterNotification</a>
 

 

