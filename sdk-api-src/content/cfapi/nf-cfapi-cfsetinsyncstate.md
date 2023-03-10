---
UID: NF:cfapi.CfSetInSyncState
title: CfSetInSyncState function (cfapi.h)
description: Sets the in-sync state for a placeholder file or folder.
helpviewer_keywords: ["CfSetInSyncState","CfSetInSyncState function","cfapi/CfSetInSyncState","cloudApi.cfsetinsyncstate"]
old-location: cloudapi\cfsetinsyncstate.htm
tech.root: cloudapi
ms.assetid: 1CB7955D-E530-4F34-8D67-BC608F8B6AF1
ms.date: 12/05/2018
ms.keywords: CfSetInSyncState, CfSetInSyncState function, cfapi/CfSetInSyncState, cloudApi.cfsetinsyncstate
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfSetInSyncState
 - cfapi/CfSetInSyncState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfSetInSyncState
---

# CfSetInSyncState function


## -description

Sets the in-sync state for a placeholder file or folder.

## -parameters

### -param FileHandle [in]

A handle to the placeholder.	The caller must have WRITE_DATA or WRITE_DAC access to the placeholder.

### -param InSyncState [in]

The in-sync state. See <a href="/windows/desktop/api/cfapi/ne-cfapi-cf_in_sync_state">CF_IN_SYNC_STATE</a> for more details.

### -param InSyncFlags [in]

The in-sync state flags. See <a href="/windows/desktop/api/cfapi/ne-cfapi-cf_set_in_sync_flags">CF_SET_IN_SYNC_FLAGS</a> for more details.

### -param InSyncUsn [in, out, optional]

This parameter needs to be a NULL pointer.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
