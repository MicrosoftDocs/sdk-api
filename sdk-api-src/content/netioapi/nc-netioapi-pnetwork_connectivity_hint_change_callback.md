---
UID: NC:netioapi.PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK
title: PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK
author: windows-sdk-content
description: An application-defined function called whenever there's a change in the network aggregate connectivity level and cost hints.
tech.root: IpHlp
ms.author: windowssdkdev
ms.date: 10/04/2019
ms.keywords: PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK, PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK callback, PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK callback function [IP Helper], netioapi.pnetwork_connectivity_hint_change_callback, netioapi/PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK
ms.topic: callback
f1_keywords: 
 - "netioapi/PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK"
req.header: netioapi.h
req.include-header: iphlpapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - netioapi.h
api_name:
 - PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

The **PNETWORK_CONNECTIVITY_HINT_CHANGE_CALLBACK** type is a pointer to a function that you define in your application. The function is called whenever there's a change in the network aggregate connectivity level and cost hints.

Register your callback with a call to [NotifyNetworkConnectivityHintChange](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange).

## -parameters

### -param CallerContext [in]

The user-specific caller context.

### -param ConnectivityHint [in]

A value of type [NL_NETWORK_CONNECTIVITY_HINT](/windows/win32/api/nldef/ns-nldef-nl_network_connectivity_hint) representing the aggregate connectivity level and cost hints.

## -remarks

## -see-also

[NotifyNetworkConnectivityHintChange](/windows/win32/api/netioapi/nf-netioapi-notifynetworkconnectivityhintchange)
