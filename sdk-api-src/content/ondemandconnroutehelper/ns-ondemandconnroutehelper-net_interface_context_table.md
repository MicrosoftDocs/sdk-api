---
UID: NS:ondemandconnroutehelper._NET_INTERFACE_CONTEXT_TABLE
title: NET_INTERFACE_CONTEXT_TABLE (ondemandconnroutehelper.h)
description: The table of NET_INTERFACE_CONTEXT structures.
helpviewer_keywords: ["NET_INTERFACE_CONTEXT_TABLE","NET_INTERFACE_CONTEXT_TABLE structure [Network Awareness]","PNET_INTERFACE_CONTEXT_TABLE","PNET_INTERFACE_CONTEXT_TABLE structure pointer [Network Awareness]","nla.net_interface_context_table","ondemandconnroutehelper/NET_INTERFACE_CONTEXT_TABLE","ondemandconnroutehelper/PNET_INTERFACE_CONTEXT_TABLE"]
old-location: nla\net_interface_context_table.htm
tech.root: nla
ms.assetid: DA6101F2-EB8F-43DC-93C6-9365A7AABEAC
ms.date: 12/05/2018
ms.keywords: NET_INTERFACE_CONTEXT_TABLE, NET_INTERFACE_CONTEXT_TABLE structure [Network Awareness], PNET_INTERFACE_CONTEXT_TABLE, PNET_INTERFACE_CONTEXT_TABLE structure pointer [Network Awareness], nla.net_interface_context_table, ondemandconnroutehelper/NET_INTERFACE_CONTEXT_TABLE, ondemandconnroutehelper/PNET_INTERFACE_CONTEXT_TABLE
req.header: ondemandconnroutehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: NET_INTERFACE_CONTEXT_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_INTERFACE_CONTEXT_TABLE
 - ondemandconnroutehelper/_NET_INTERFACE_CONTEXT_TABLE
 - NET_INTERFACE_CONTEXT_TABLE
 - ondemandconnroutehelper/NET_INTERFACE_CONTEXT_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OnDemandConnRouteHelper.h
api_name:
 - NET_INTERFACE_CONTEXT_TABLE
---

# NET_INTERFACE_CONTEXT_TABLE structure


## -description

The table of <a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT</a> structures.

## -struct-fields

### -field InterfaceContextHandle

A handle to the interface context.

### -field NumberOfEntries

The number of entries in the table.

### -field InterfaceContextArray

An array of <a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT</a> structures.

## -see-also

<a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname">GetInterfaceContextTableForHostName</a>



<a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT</a>