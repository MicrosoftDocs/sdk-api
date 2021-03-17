---
UID: NS:windns._MDNS_QUERY_HANDLE
title: MDNS_QUERY_HANDLE structure
description: Contains information related to an ongoing MDNS query. Your application must not modify its contents.
tech.root: dns
helpviewer_keywords: ["_MDNS_QUERY_HANDLE","MDNS_QUERY_HANDLE"]
ms.date: 02/19/2019
ms.keywords: _MDNS_QUERY_HANDLE, MDNS_QUERY_HANDLE
targetos: Windows
req.assembly: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.typenames: MDNS_QUERY_HANDLE, *PMDNS_QUERY_HANDLE
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - _MDNS_QUERY_HANDLE
 - windns/_MDNS_QUERY_HANDLE
 - PMDNS_QUERY_HANDLE
 - windns/PMDNS_QUERY_HANDLE
 - MDNS_QUERY_HANDLE
 - windns/MDNS_QUERY_HANDLE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _MDNS_QUERY_HANDLE
 - MDNS_QUERY_HANDLE
---

## -description

Contains information related to an ongoing MDNS query. Your application must not modify its contents.

## -struct-fields

### -field nameBuf

A value representing the queried name.

### -field wType

A value representing the type of the query.

### -field pSubscription

Reserved. Do not use.

### -field pWnfCallbackParams

Reserved. Do not use.

### -field stateNameData

Reserved. Do not use.

## -remarks

This structure is for internal use only.

## -see-also

