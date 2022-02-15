---
UID: NE:tspubplugin2com._TSPUB_PLUGIN_PD_RESOLUTION_TYPE
title: TSPUB_PLUGIN_PD_RESOLUTION_TYPE (tspubplugin2com.h)
description: Specifies the type of personal desktop resolution being requested.
helpviewer_keywords: ["TSPUB_PLUGIN_PD_QUERY_EXISTING","TSPUB_PLUGIN_PD_QUERY_OR_CREATE","TSPUB_PLUGIN_PD_RESOLUTION_TYPE","TSPUB_PLUGIN_PD_RESOLUTION_TYPE enumeration [Remote Desktop Services]","termserv.tspub_plugin_pd_resolution_type","tspubplugin2com/TSPUB_PLUGIN_PD_QUERY_EXISTING","tspubplugin2com/TSPUB_PLUGIN_PD_QUERY_OR_CREATE","tspubplugin2com/TSPUB_PLUGIN_PD_RESOLUTION_TYPE"]
old-location: termserv\tspub_plugin_pd_resolution_type.htm
tech.root: TermServ
ms.assetid: 8cba4e6a-3508-4f9f-a206-4a0b41a933c1
ms.date: 12/05/2018
ms.keywords: TSPUB_PLUGIN_PD_QUERY_EXISTING, TSPUB_PLUGIN_PD_QUERY_OR_CREATE, TSPUB_PLUGIN_PD_RESOLUTION_TYPE, TSPUB_PLUGIN_PD_RESOLUTION_TYPE enumeration [Remote Desktop Services], termserv.tspub_plugin_pd_resolution_type, tspubplugin2com/TSPUB_PLUGIN_PD_QUERY_EXISTING, tspubplugin2com/TSPUB_PLUGIN_PD_QUERY_OR_CREATE, tspubplugin2com/TSPUB_PLUGIN_PD_RESOLUTION_TYPE
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
targetos: Windows
req.typenames: TSPUB_PLUGIN_PD_RESOLUTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TSPUB_PLUGIN_PD_RESOLUTION_TYPE
 - tspubplugin2com/_TSPUB_PLUGIN_PD_RESOLUTION_TYPE
 - TSPUB_PLUGIN_PD_RESOLUTION_TYPE
 - tspubplugin2com/TSPUB_PLUGIN_PD_RESOLUTION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tspubplugin2com.h
api_name:
 - TSPUB_PLUGIN_PD_RESOLUTION_TYPE
---

# TSPUB_PLUGIN_PD_RESOLUTION_TYPE enumeration


## -description

Specifies the type of personal desktop resolution being requested.

## -enum-fields

### -field TSPUB_PLUGIN_PD_QUERY_OR_CREATE:0

Resolve an existing personal desktop for the user. If no personal desktop exists, the <a href="/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-resolvepersonaldesktop">ResolvePersonalDesktop</a> method should create a new one.

### -field TSPUB_PLUGIN_PD_QUERY_EXISTING:1

Resolve an existing personal desktop for the user. If no personal desktop exists, the <a href="/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-resolvepersonaldesktop">ResolvePersonalDesktop</a> method should return an error code.

## -see-also

<a href="/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-resolvepersonaldesktop">ResolvePersonalDesktop</a>
