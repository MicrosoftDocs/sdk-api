---
UID: NF:shobjidl_core.ISharingConfigurationManager.DeleteShare
title: ISharingConfigurationManager::DeleteShare (shobjidl_core.h)
description: Removes sharing from either the Users or Public folder.
helpviewer_keywords: ["DeleteShare","DeleteShare method [Windows Shell]","DeleteShare method [Windows Shell]","ISharingConfigurationManager interface","ISharingConfigurationManager interface [Windows Shell]","DeleteShare method","ISharingConfigurationManager.DeleteShare","ISharingConfigurationManager::DeleteShare","_shell_ISharingConfigurationManager_DeleteShare","shell.ISharingConfigurationManager_DeleteShare","shobjidl_core/ISharingConfigurationManager::DeleteShare"]
old-location: shell\ISharingConfigurationManager_DeleteShare.htm
tech.root: shell
ms.assetid: 8b78d321-0da6-4b7e-8408-34784d309a1b
ms.date: 12/05/2018
ms.keywords: DeleteShare, DeleteShare method [Windows Shell], DeleteShare method [Windows Shell],ISharingConfigurationManager interface, ISharingConfigurationManager interface [Windows Shell],DeleteShare method, ISharingConfigurationManager.DeleteShare, ISharingConfigurationManager::DeleteShare, _shell_ISharingConfigurationManager_DeleteShare, shell.ISharingConfigurationManager_DeleteShare, shobjidl_core/ISharingConfigurationManager::DeleteShare
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISharingConfigurationManager::DeleteShare
 - shobjidl_core/ISharingConfigurationManager::DeleteShare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ISharingConfigurationManager.DeleteShare
---

# ISharingConfigurationManager::DeleteShare


## -description

Removes sharing from either the <b>Users</b> or <b>Public</b> folder.

## -parameters

### -param dsid [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id">DEF_SHARE_ID</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id">DEF_SHARE_ID</a> values that specifies the folder to no longer share.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Running this method requires an Administrator privilege level.