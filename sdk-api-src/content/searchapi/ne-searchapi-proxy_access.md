---
UID: NE:searchapi._PROXY_ACCESS
title: PROXY_ACCESS (searchapi.h)
description: Used by ISearchManager to state proxy use.
helpviewer_keywords: ["PROXY_ACCESS","PROXY_ACCESS enumeration [search]","PROXY_ACCESS_DIRECT","PROXY_ACCESS_PRECONFIG","PROXY_ACCESS_PROXY","_search_PROXY_ACCESS","search._search_PROXY_ACCESS","searchapi/PROXY_ACCESS","searchapi/PROXY_ACCESS_DIRECT","searchapi/PROXY_ACCESS_PRECONFIG","searchapi/PROXY_ACCESS_PROXY"]
old-location: search\_search_PROXY_ACCESS.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\proxy_access.htm
ms.date: 12/05/2018
ms.keywords: PROXY_ACCESS, PROXY_ACCESS enumeration [search], PROXY_ACCESS_DIRECT, PROXY_ACCESS_PRECONFIG, PROXY_ACCESS_PROXY, _search_PROXY_ACCESS, search._search_PROXY_ACCESS, searchapi/PROXY_ACCESS, searchapi/PROXY_ACCESS_DIRECT, searchapi/PROXY_ACCESS_PRECONFIG, searchapi/PROXY_ACCESS_PROXY
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
req.typenames: PROXY_ACCESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROXY_ACCESS
 - searchapi/_PROXY_ACCESS
 - PROXY_ACCESS
 - searchapi/PROXY_ACCESS
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
 - PROXY_ACCESS
---

# PROXY_ACCESS enumeration


## -description

Used by <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchmanager">ISearchManager</a> to state proxy use.

## -enum-fields

### -field PROXY_ACCESS_PRECONFIG:0

Use proxy as set by Internet settings.

### -field PROXY_ACCESS_DIRECT

Do not use a proxy.

### -field PROXY_ACCESS_PROXY

Use the specified proxy.
