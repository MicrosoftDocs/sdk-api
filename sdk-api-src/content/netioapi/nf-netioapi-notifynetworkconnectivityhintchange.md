---
UID: NF:netioapi.NotifyNetworkConnectivityHintChange
title: NotifyNetworkConnectivityHintChange
author: windows-sdk-content
description: Registers an application-defined callback function, to be called when the aggregate network connectivity level and cost hints change.
tech.root: IpHlp
ms.author: windowssdkdev
ms.date: 10/04/2019
ms.keywords: NotifyNetworkConnectivityHintChange, NotifyNetworkConnectivityHintChange function [IP Helper], netioapi.NotifyNetworkConnectivityHintChange, netioapi/NotifyNetworkConnectivityHintChange
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - NotifyNetworkConnectivityHintChange
 - netioapi/NotifyNetworkConnectivityHintChange
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - NotifyNetworkConnectivityHintChange
---

## -description

Registers an application-defined callback function, to be called when the aggregate network connectivity level and cost hints change.

## -parameters

### -param Callback [in]

A function pointer of type [PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK](./nc-netioapi-pnetwork_connectivity_hint_change_callback.md), which points to your application-defined callback function. The callback function will be invoked when a network connectivity level or cost change occurs.

### -param CallerContext [in]

The user-specific caller context. This context will be supplied to the callback function.

### -param InitialNotification [in]

`True` if an initialization notification should be provided, otherwise `false`.

### -param NotificationHandle [out]

A pointer to a **HANDLE**. The function sets the value to a handle to the notification registration.

## -returns

If the function succeeds, the return value is **NO_ERROR**. Otherwise, an error code is returned.

## -remarks

To deregister for change notifications, call the **CancelMibChangeNotify2** function, passing the *NotificationHandle* parameter returned by **NotifyNetworkConnectivityHintChange**.

## -see-also

* [PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK](./nc-netioapi-pnetwork_connectivity_hint_change_callback.md)

* [CancelMibChangeNotify2](./nf-netioapi-cancelmibchangenotify2.md)
