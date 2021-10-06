---
UID: NE:clusapi._FILESHARE_CHANGE_ENUM
title: FILESHARE_CHANGE_ENUM (clusapi.h)
description: Contains the possible change events that are used by the FILESHARE_CHANGE structure to describe an entry in a file share event notification list.
helpviewer_keywords: ["*PFILESHARE_CHANGE_ENUM","FILESHARE_CHANGE_ADD","FILESHARE_CHANGE_DEL","FILESHARE_CHANGE_ENUM","FILESHARE_CHANGE_ENUM enumeration [Failover Cluster]","FILESHARE_CHANGE_MODIFY","FILESHARE_CHANGE_NONE","clusapi/FILESHARE_CHANGE_ADD","clusapi/FILESHARE_CHANGE_DEL","clusapi/FILESHARE_CHANGE_ENUM","clusapi/FILESHARE_CHANGE_MODIFY","clusapi/FILESHARE_CHANGE_NONE","mscs.fileshare_change_enum"]
old-location: mscs\fileshare_change_enum.htm
tech.root: MsCS
ms.assetid: 36139a95-141c-4f44-9627-9ed6c3fed0c5
ms.date: 12/05/2018
ms.keywords: '*PFILESHARE_CHANGE_ENUM, FILESHARE_CHANGE_ADD, FILESHARE_CHANGE_DEL, FILESHARE_CHANGE_ENUM, FILESHARE_CHANGE_ENUM enumeration [Failover Cluster], FILESHARE_CHANGE_MODIFY, FILESHARE_CHANGE_NONE, clusapi/FILESHARE_CHANGE_ADD, clusapi/FILESHARE_CHANGE_DEL, clusapi/FILESHARE_CHANGE_ENUM, clusapi/FILESHARE_CHANGE_MODIFY, clusapi/FILESHARE_CHANGE_NONE, mscs.fileshare_change_enum'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: FILESHARE_CHANGE_ENUM, *PFILESHARE_CHANGE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILESHARE_CHANGE_ENUM
 - clusapi/_FILESHARE_CHANGE_ENUM
 - PFILESHARE_CHANGE_ENUM
 - clusapi/PFILESHARE_CHANGE_ENUM
 - FILESHARE_CHANGE_ENUM
 - clusapi/FILESHARE_CHANGE_ENUM
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
 - FILESHARE_CHANGE_ENUM
---

# FILESHARE_CHANGE_ENUM enumeration


## -description

Contains the possible change events that are used by the 
    <a href="/windows/desktop/api/clusapi/ns-clusapi-fileshare_change">FILESHARE_CHANGE</a> structure to describe an entry in a 
    file share event notification list.

## -enum-fields

### -field FILESHARE_CHANGE_NONE

This is a place holder value and is not a valid event.

### -field FILESHARE_CHANGE_ADD

A new file share resource has been created and will be included with the other file shares managed by the 
       File Server resource.

### -field FILESHARE_CHANGE_DEL

A file share resource has been deleted and will be removed from the file shares managed by the File Server 
       resource.

### -field FILESHARE_CHANGE_MODIFY

One or more properties of an existing file share resource have been changed.

## -remarks

<b>NNLEN</b> is defined by ClusAPI.h as follows.


``` syntax
#define NNLEN       80                  // Net name length (share name)
```


## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-fileshare_change">FILESHARE_CHANGE</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
