---
UID: NF:shobjidl_core.ISharingConfigurationManager.GetSharePermissions
title: ISharingConfigurationManager::GetSharePermissions (shobjidl_core.h)
description: Gets the access permissions currently associated with the User or Public folder for the Everyone access control entry (ACE).
helpviewer_keywords: ["GetSharePermissions","GetSharePermissions method [Windows Shell]","GetSharePermissions method [Windows Shell]","ISharingConfigurationManager interface","ISharingConfigurationManager interface [Windows Shell]","GetSharePermissions method","ISharingConfigurationManager.GetSharePermissions","ISharingConfigurationManager::GetSharePermissions","_shell_ISharingConfigurationManager_GetSharePermissions","shell.ISharingConfigurationManager_GetSharePermissions","shobjidl_core/ISharingConfigurationManager::GetSharePermissions"]
old-location: shell\ISharingConfigurationManager_GetSharePermissions.htm
tech.root: shell
ms.assetid: d9ca5acf-2dd1-4fbe-a67f-91578d68b955
ms.date: 12/05/2018
ms.keywords: GetSharePermissions, GetSharePermissions method [Windows Shell], GetSharePermissions method [Windows Shell],ISharingConfigurationManager interface, ISharingConfigurationManager interface [Windows Shell],GetSharePermissions method, ISharingConfigurationManager.GetSharePermissions, ISharingConfigurationManager::GetSharePermissions, _shell_ISharingConfigurationManager_GetSharePermissions, shell.ISharingConfigurationManager_GetSharePermissions, shobjidl_core/ISharingConfigurationManager::GetSharePermissions
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
 - ISharingConfigurationManager::GetSharePermissions
 - shobjidl_core/ISharingConfigurationManager::GetSharePermissions
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
 - ISharingConfigurationManager.GetSharePermissions
---

# ISharingConfigurationManager::GetSharePermissions


## -description

Gets the access permissions currently associated with the <b>User</b> or <b>Public</b> folder for the <i>Everyone</i> access control entry (ACE).

## -parameters

### -param dsid [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id">DEF_SHARE_ID</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id">DEF_SHARE_ID</a> values that specifies the folder.

### -param pRole [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role">SHARE_ROLE</a>*</b>

A pointer to a value that, when this method returns successfully, receives one of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role">SHARE_ROLE</a> values that indicate the sharing permissions set for the folder specified in the <i>dsid</i> parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.