---
UID: NS:winsvc._SERVICE_PREFERRED_NODE_INFO
title: SERVICE_PREFERRED_NODE_INFO (winsvc.h)
description: Represents the preferred node on which to run a service.
helpviewer_keywords: ["*LPSERVICE_PREFERRED_NODE_INFO","LPSERVICE_PREFERRED_NODE_INFO","LPSERVICE_PREFERRED_NODE_INFO structure pointer","SERVICE_PREFERRED_NODE_INFO","SERVICE_PREFERRED_NODE_INFO structure","base.service_preferred_node_info","winsvc/LPSERVICE_PREFERRED_NODE_INFO","winsvc/SERVICE_PREFERRED_NODE_INFO"]
old-location: base\service_preferred_node_info.htm
tech.root: security
ms.assetid: aa16cc56-0a95-47e0-9390-c219b83aeeb4
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_PREFERRED_NODE_INFO, LPSERVICE_PREFERRED_NODE_INFO, LPSERVICE_PREFERRED_NODE_INFO structure pointer, SERVICE_PREFERRED_NODE_INFO, SERVICE_PREFERRED_NODE_INFO structure, base.service_preferred_node_info, winsvc/LPSERVICE_PREFERRED_NODE_INFO, winsvc/SERVICE_PREFERRED_NODE_INFO'
req.header: winsvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SERVICE_PREFERRED_NODE_INFO, *LPSERVICE_PREFERRED_NODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_PREFERRED_NODE_INFO
 - winsvc/_SERVICE_PREFERRED_NODE_INFO
 - LPSERVICE_PREFERRED_NODE_INFO
 - winsvc/LPSERVICE_PREFERRED_NODE_INFO
 - SERVICE_PREFERRED_NODE_INFO
 - winsvc/SERVICE_PREFERRED_NODE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsvc.h
api_name:
 - SERVICE_PREFERRED_NODE_INFO
---

# SERVICE_PREFERRED_NODE_INFO structure


## -description

Represents the preferred node on which to run a service.

## -struct-fields

### -field usPreferredNode

The node number of the preferred node.

### -field fDelete

If this member is TRUE, the preferred node setting is deleted.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/ProcThread/numa-support">NUMA Support</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>