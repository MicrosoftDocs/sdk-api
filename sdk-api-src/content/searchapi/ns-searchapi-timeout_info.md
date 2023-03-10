---
UID: NS:searchapi._TIMEOUT_INFO
title: TIMEOUT_INFO (searchapi.h)
description: Stores time-out values for connections and data.
helpviewer_keywords: ["TIMEOUT_INFO","TIMEOUT_INFO structure [search]","_search_TIMEOUT_INFO","search._search_TIMEOUT_INFO","searchapi/TIMEOUT_INFO"]
old-location: search\_search_TIMEOUT_INFO.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\timeout_info.htm
ms.date: 12/05/2018
ms.keywords: TIMEOUT_INFO, TIMEOUT_INFO structure [search], _search_TIMEOUT_INFO, search._search_TIMEOUT_INFO, searchapi/TIMEOUT_INFO
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TIMEOUT_INFO
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _TIMEOUT_INFO
 - searchapi/_TIMEOUT_INFO
 - TIMEOUT_INFO
 - searchapi/TIMEOUT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - TIMEOUT_INFO
---

# TIMEOUT_INFO structure


## -description

Stores time-out values for connections and data.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of the structure, in bytes.

### -field dwConnectTimeout

Type: <b>DWORD</b>

The time-out value for a connection, in seconds.

### -field dwDataTimeout

Type: <b>DWORD</b>

The time-out value for data, in seconds.

