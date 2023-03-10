---
UID: NE:projectedfslib.PRJ_STARTVIRTUALIZING_FLAGS
title: PRJ_STARTVIRTUALIZING_FLAGS (projectedfslib.h)
description: Flags to provide when starting a virtualization instance.
helpviewer_keywords: ["PRJ_FLAG_NONE","PRJ_FLAG_USE_NEGATIVE_PATH_CACHE","PRJ_STARTVIRTUALIZING_FLAGS","PRJ_STARTVIRTUALIZING_FLAGS enumeration","ProjFS.prj_startvirtualizing_flags","projectedfslib/PRJ_FLAG_NONE","projectedfslib/PRJ_FLAG_USE_NEGATIVE_PATH_CACHE","projectedfslib/PRJ_STARTVIRTUALIZING_FLAGS"]
old-location: projfs\prj_startvirtualizing_flags.htm
tech.root: ProjFS
ms.assetid: AF67668B-E9BC-4320-AB1F-1E78CA700D8E
ms.date: 12/05/2018
ms.keywords: PRJ_FLAG_NONE, PRJ_FLAG_USE_NEGATIVE_PATH_CACHE, PRJ_STARTVIRTUALIZING_FLAGS, PRJ_STARTVIRTUALIZING_FLAGS enumeration, ProjFS.prj_startvirtualizing_flags, projectedfslib/PRJ_FLAG_NONE, projectedfslib/PRJ_FLAG_USE_NEGATIVE_PATH_CACHE, projectedfslib/PRJ_STARTVIRTUALIZING_FLAGS
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_STARTVIRTUALIZING_FLAGS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_STARTVIRTUALIZING_FLAGS
 - projectedfslib/PRJ_STARTVIRTUALIZING_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_STARTVIRTUALIZING_FLAGS
---

# PRJ_STARTVIRTUALIZING_FLAGS enumeration


## -description

Flags to provide when starting a virtualization instance.

## -enum-fields

### -field PRJ_FLAG_NONE:0x00000000

No flags.

### -field PRJ_FLAG_USE_NEGATIVE_PATH_CACHE:0x00000001

Specifies that ProjFS should maintain a "negative path cache" for the virtualization instance. If the negative path cache is active, then if the provider indicates that a file path does not exist by returning HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) from its <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback, ProjFS will fail subsequent opens of that path without calling the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> callback again. 

To resume receiving the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb">PRJ_GET_PLACEHOLDER_INFO_CB</a> for paths the provider has indicated do not exist, the provider must call <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache">PrjClearNegativePathCache</a>.
