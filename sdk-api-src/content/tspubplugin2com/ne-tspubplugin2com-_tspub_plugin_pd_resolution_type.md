---
UID: NE:tspubplugin2com._TSPUB_PLUGIN_PD_RESOLUTION_TYPE
title: "_TSPUB_PLUGIN_PD_RESOLUTION_TYPE"
author: windows-sdk-content
description: Specifies the type of personal desktop resolution being requested.
old-location: termserv\tspub_plugin_pd_resolution_type.htm
tech.root: termserv
ms.assetid: 8cba4e6a-3508-4f9f-a206-4a0b41a933c1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TSPUB_PLUGIN_PD_QUERY_EXISTING, TSPUB_PLUGIN_PD_QUERY_OR_CREATE, TSPUB_PLUGIN_PD_RESOLUTION_TYPE, TSPUB_PLUGIN_PD_RESOLUTION_TYPE enumeration [Remote Desktop Services], _TSPUB_PLUGIN_PD_RESOLUTION_TYPE, termserv.tspub_plugin_pd_resolution_type, tspubplugin2com/TSPUB_PLUGIN_PD_QUERY_EXISTING, tspubplugin2com/TSPUB_PLUGIN_PD_QUERY_OR_CREATE, tspubplugin2com/TSPUB_PLUGIN_PD_RESOLUTION_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tspubplugin2com.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tspubplugin2com.idl
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
 - tspubplugin2com.h
api_name:
 - TSPUB_PLUGIN_PD_RESOLUTION_TYPE
product: Windows
targetos: Windows
req.typenames: TSPUB_PLUGIN_PD_RESOLUTION_TYPE
req.redist: 
---

# _TSPUB_PLUGIN_PD_RESOLUTION_TYPE enumeration


## -description


Specifies the type of personal desktop resolution being requested.


## -enum-fields




### -field TSPUB_PLUGIN_PD_QUERY_OR_CREATE

Resolve an existing personal desktop for the user. If no personal desktop exists, the <a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a> method should create a new one.


### -field TSPUB_PLUGIN_PD_QUERY_EXISTING

Resolve an existing personal desktop for the user. If no personal desktop exists, the <a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a> method should return an error code.


## -see-also




<a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a>
 

 

