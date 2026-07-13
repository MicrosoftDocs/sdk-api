---
UID: NF:searchapi.ISearchCatalogManager3.IsContainsSemanticSupported
tech.root: search
title: ISearchCatalogManager3::IsContainsSemanticSupported
ms.date: 04/17/2025
targetos: Windows
description: Returns a Boolean value that indicates whether the CONTAINSSEMANTIC SQL predicate is supported on the current device.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: searchapi.h
req.idl: Searchcatalog.idl
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, build 26100
req.target-min-winversvr: Windows Server 2025, build 26100
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchCatalogManager3::IsContainsSemanticSupported
f1_keywords:
 - ISearchCatalogManager3::IsContainsSemanticSupported
 - searchapi/ISearchCatalogManager3::IsContainsSemanticSupported
dev_langs:
 - c++
helpviewer_keywords:
 - IsContainsSemanticSupported
---

## -description

Returns a Boolean value that indicates whether the [CONTAINSSEMANTIC](/windows/win32/search/-search-sql-containssemantic) SQL predicate is supported on the current device.

## -parameters

### -param isContainsSemanticSupported [out]

TRUE if semantic SQL predicates are supported on the current device; otherwise, FALSE.

## -returns

Returns S_OK on success. Otherwise it returns an error code.

## -remarks

Starting with Windows 11, build 26100, Windows Search queries can include new SQL syntax that enables searching for semantically-related items. The semantic search syntax includes the **CONTAINSSEMANTIC** predicate and [MERGE](/windows/win32/search/-search-sql-rankby#mergemerge_operation) operations. Older versions of Windows do not support this syntax. **IsContainsSemanticSupported** allows apps to confirm that **CONTAINSSEMANTIC** is supported on the current device before executing queries that use this predicate.

## -see-also

