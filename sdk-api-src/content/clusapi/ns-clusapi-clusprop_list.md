---
UID: NS:clusapi.CLUSPROP_LIST
title: CLUSPROP_LIST (clusapi.h)
description: Accesses the beginning of a property list.
helpviewer_keywords: ["*PCLUSPROP_LIST","CLUSPROP_LIST","CLUSPROP_LIST structure [Failover Cluster]","PCLUSPROP_LIST","PCLUSPROP_LIST structure pointer [Failover Cluster]","_wolf_clusprop_list","clusapi/CLUSPROP_LIST","clusapi/PCLUSPROP_LIST","mscs.clusprop_list"]
old-location: mscs\clusprop_list.htm
tech.root: MsCS
ms.assetid: 1f76104f-99eb-4376-8d92-e04b7f00c46d
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_LIST, CLUSPROP_LIST, CLUSPROP_LIST structure [Failover Cluster], PCLUSPROP_LIST, PCLUSPROP_LIST structure pointer [Failover Cluster], _wolf_clusprop_list, clusapi/CLUSPROP_LIST, clusapi/PCLUSPROP_LIST, mscs.clusprop_list'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUSPROP_LIST, *PCLUSPROP_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_LIST
 - clusapi/CLUSPROP_LIST
 - PCLUSPROP_LIST
 - clusapi/PCLUSPROP_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_LIST
---

# CLUSPROP_LIST structure


## -description

Accesses the beginning of a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>.

## -struct-fields

### -field nPropertyCount

Number of properties in the property list.

### -field PropertyName

Structure describing the name of the first property in the list.

## -remarks

For information about property lists, see  <a href="/previous-versions/windows/desktop/mscs/property-lists">Property Lists</a>.