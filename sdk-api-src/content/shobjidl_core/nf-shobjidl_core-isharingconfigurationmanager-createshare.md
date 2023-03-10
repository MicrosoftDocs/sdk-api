---
UID: NF:shobjidl_core.ISharingConfigurationManager.CreateShare
title: ISharingConfigurationManager::CreateShare (shobjidl_core.h)
description: Shares the Users or Public folder. If the folder is already shared, this method updates its sharing status.
helpviewer_keywords: ["CreateShare","CreateShare method [Windows Shell]","CreateShare method [Windows Shell]","ISharingConfigurationManager interface","ISharingConfigurationManager interface [Windows Shell]","CreateShare method","ISharingConfigurationManager.CreateShare","ISharingConfigurationManager::CreateShare","SHARE_ROLE_CO_OWNER","SHARE_ROLE_READER","_shell_ISharingConfigurationManager_CreateShare","shell.ISharingConfigurationManager_CreateShare","shobjidl_core/ISharingConfigurationManager::CreateShare"]
old-location: shell\ISharingConfigurationManager_CreateShare.htm
tech.root: shell
ms.assetid: 81bcd470-3fb8-4c6d-af4f-6f11206fa40a
ms.date: 12/05/2018
ms.keywords: CreateShare, CreateShare method [Windows Shell], CreateShare method [Windows Shell],ISharingConfigurationManager interface, ISharingConfigurationManager interface [Windows Shell],CreateShare method, ISharingConfigurationManager.CreateShare, ISharingConfigurationManager::CreateShare, SHARE_ROLE_CO_OWNER, SHARE_ROLE_READER, _shell_ISharingConfigurationManager_CreateShare, shell.ISharingConfigurationManager_CreateShare, shobjidl_core/ISharingConfigurationManager::CreateShare
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
 - ISharingConfigurationManager::CreateShare
 - shobjidl_core/ISharingConfigurationManager::CreateShare
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
 - ISharingConfigurationManager.CreateShare
---

# ISharingConfigurationManager::CreateShare


## -description

Shares the <b>Users</b> or <b>Public</b> folder. If the folder is already shared, this method updates its sharing status.

## -parameters

### -param dsid [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id">DEF_SHARE_ID</a></b>

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id">DEF_SHARE_ID</a> values that indicates the folder to share or update.

### -param role [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role">SHARE_ROLE</a></b>

One of the following <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role">SHARE_ROLE</a> values that sets the access permissions of the share for the <i>Everyone</i> ACE. <b>CreateShare</b> accepts only these values.





#### SHARE_ROLE_READER (0)

Read-only. The contents of the folder can be read, but not altered or added to.



#### SHARE_ROLE_CO_OWNER (2)

Read/Write. The contents of the folder can be read, changed, or added to.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>role</i> parameter specifies a value other than SHARE_ROLE_READER or SHARE_ROLE_CO_OWNER.

</td>
</tr>
</table>

## -remarks

Running this method requires an Administrator privilege level.

If the folder named in <i>dsid</i> is not shared, this method shares the folder using the permission level provided in the <i>role</i> parameter.

If the folder named in <i>dsid</i> is already shared, this method updates the permissions on the share with the value provided in the <i>role</i> parameter.

Because as of Windows 7 the <b>Public</b> folder is shared through <b>Users</b> rather than directly, creating a share on <b>Public</b> causes an Server Message Block (SMB) share to be created on <b>Users</b>.