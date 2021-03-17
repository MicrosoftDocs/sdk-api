---
UID: NS:searchapi._INCREMENTAL_ACCESS_INFO
title: INCREMENTAL_ACCESS_INFO (searchapi.h)
description: Contains access information used by an incremental crawl, such as the last access date and modification time.
helpviewer_keywords: ["INCREMENTAL_ACCESS_INFO","INCREMENTAL_ACCESS_INFO structure [search]","_search_INCREMENTAL_ACCESS_INFO","search._search_INCREMENTAL_ACCESS_INFO","searchapi/INCREMENTAL_ACCESS_INFO"]
old-location: search\_search_INCREMENTAL_ACCESS_INFO.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\incremental_access_info.htm
ms.date: 12/05/2018
ms.keywords: INCREMENTAL_ACCESS_INFO, INCREMENTAL_ACCESS_INFO structure [search], _search_INCREMENTAL_ACCESS_INFO, search._search_INCREMENTAL_ACCESS_INFO, searchapi/INCREMENTAL_ACCESS_INFO
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
req.typenames: INCREMENTAL_ACCESS_INFO
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _INCREMENTAL_ACCESS_INFO
 - searchapi/_INCREMENTAL_ACCESS_INFO
 - INCREMENTAL_ACCESS_INFO
 - searchapi/INCREMENTAL_ACCESS_INFO
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
 - INCREMENTAL_ACCESS_INFO
---

# INCREMENTAL_ACCESS_INFO structure


## -description

Contains access information used by an incremental crawl, such as the last access date and modification time.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

Size of the file in bytes.

### -field ftLastModifiedTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

Last time the file was modified.