---
UID: NS:ondemandconnroutehelper._NET_INTERFACE_CONTEXT_TABLE
title: NET_INTERFACE_CONTEXT_TABLE
author: windows-sdk-content
description: The table of NET_INTERFACE_CONTEXT structures.
old-location: nla\net_interface_context_table.htm
tech.root: nla
ms.assetid: DA6101F2-EB8F-43DC-93C6-9365A7AABEAC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NET_INTERFACE_CONTEXT_TABLE, NET_INTERFACE_CONTEXT_TABLE structure [Network Awareness], PNET_INTERFACE_CONTEXT_TABLE, PNET_INTERFACE_CONTEXT_TABLE structure pointer [Network Awareness], nla.net_interface_context_table, ondemandconnroutehelper/NET_INTERFACE_CONTEXT_TABLE, ondemandconnroutehelper/PNET_INTERFACE_CONTEXT_TABLE
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OnDemandConnRouteHelper.h
api_name:
 - NET_INTERFACE_CONTEXT_TABLE
product: Windows
targetos: Windows
req.typenames: NET_INTERFACE_CONTEXT_TABLE
req.redist: 
---

# NET_INTERFACE_CONTEXT_TABLE structure


## -description


The table of <a href="https://msdn.microsoft.com/en-us/library/Mt162305(v=VS.85).aspx">NET_INTERFACE_CONTEXT</a> structures.


## -struct-fields




### -field InterfaceContextHandle

A handle to the interface context.


### -field NumberOfEntries

The number of entries in the table.


### -field InterfaceContextArray

An array of <a href="https://msdn.microsoft.com/en-us/library/Mt162305(v=VS.85).aspx">NET_INTERFACE_CONTEXT</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/BD687853-6242-4A72-BACE-13B681FD4674">GetInterfaceContextTableForHostName</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt162305(v=VS.85).aspx">NET_INTERFACE_CONTEXT</a>
 

 

