---
UID: NF:netioapi.GetNetworkConnectivityHint
title: GetNetworkConnectivityHint
author: windows-sdk-content
description: Retrieves the aggregate level and cost of network connectivity that an application or service is likely to experience.
tech.root: IpHlp
ms.author: windowssdkdev
ms.date: 10/04/2019
ms.keywords: GetNetworkConnectivityHint, GetNetworkConnectivityHint function [IP Helper], netioapi.GetNetworkConnectivityHint, netioapi/GetNetworkConnectivityHint
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
 - GetNetworkConnectivityHint
 - netioapi/GetNetworkConnectivityHint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetNetworkConnectivityHint
---

## -description

Retrieves the aggregate level and cost of network connectivity that an application or service is likely to experience.

## -parameters

### -param ConnectivityHint [out]

A pointer to a value of type [NL_NETWORK_CONNECTIVITY_HINT](../nldef/ns-nldef-nl_network_connectivity_hint.md). The function sets this value to the aggregate connectivity level and cost hints.

## -returns

In user mode, returns **NO_ERROR** on success, and a Win32 error code on failure. In kernel mode, returns **STATUS_SUCCESS** on success, and an NTSTATUS error code on failure.

## -remarks

## -see-also