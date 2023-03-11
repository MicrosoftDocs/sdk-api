---
UID: NE:shobjidl_core._KF_DEFINITION_FLAGS
title: _KF_DEFINITION_FLAGS (shobjidl_core.h)
description: Flags that specify certain known folder behaviors. Used with the KNOWNFOLDER_DEFINITION structure.
helpviewer_keywords: ["KFDF_LOCAL_REDIRECT_ONLY","KFDF_NO_REDIRECT_UI","KFDF_PRECREATE","KFDF_PUBLISHEXPANDEDPATH","KFDF_ROAMABLE","KFDF_STREAM","KF_DEFINITION_FLAGS","KF_DEFINITION_FLAGS enumeration [Windows Shell]","_KF_DEFINITION_FLAGS","_shell_KF_DEFINITION_FLAGS","shell.KF_DEFINITION_FLAGS","shobjidl_core/KFDF_LOCAL_REDIRECT_ONLY","shobjidl_core/KFDF_NO_REDIRECT_UI","shobjidl_core/KFDF_PRECREATE","shobjidl_core/KFDF_PUBLISHEXPANDEDPATH","shobjidl_core/KFDF_ROAMABLE","shobjidl_core/KFDF_STREAM","shobjidl_core/KF_DEFINITION_FLAGS"]
old-location: shell\KF_DEFINITION_FLAGS.htm
tech.root: shell
ms.assetid: c5267aea-19b7-4e4a-a443-24674a6ae608
ms.date: 12/05/2018
ms.keywords: KFDF_LOCAL_REDIRECT_ONLY, KFDF_NO_REDIRECT_UI, KFDF_PRECREATE, KFDF_PUBLISHEXPANDEDPATH, KFDF_ROAMABLE, KFDF_STREAM, KF_DEFINITION_FLAGS, KF_DEFINITION_FLAGS enumeration [Windows Shell], _KF_DEFINITION_FLAGS, _shell_KF_DEFINITION_FLAGS, shell.KF_DEFINITION_FLAGS, shobjidl_core/KFDF_LOCAL_REDIRECT_ONLY, shobjidl_core/KFDF_NO_REDIRECT_UI, shobjidl_core/KFDF_PRECREATE, shobjidl_core/KFDF_PUBLISHEXPANDEDPATH, shobjidl_core/KFDF_ROAMABLE, shobjidl_core/KFDF_STREAM, shobjidl_core/KF_DEFINITION_FLAGS
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - _KF_DEFINITION_FLAGS
 - shobjidl_core/_KF_DEFINITION_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - KF_DEFINITION_FLAGS
---

# _KF_DEFINITION_FLAGS enumeration


## -description

Flags that specify certain known folder behaviors. Used with the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a> structure.

## -enum-fields

### -field KFDF_LOCAL_REDIRECT_ONLY:0x2

Prevent a <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">per-user</a> known folder from being redirected to a network location. Note that if the known folder has been flagged with KFDF_LOCAL_REDIRECT_ONLY but it is a subfolder of a known folder that is redirected to a network location, this subfolder is redirected also.

### -field KFDF_ROAMABLE:0x4

Can be roamed through a PC-to-PC synchronization.

### -field KFDF_PRECREATE:0x8

Create the folder when the user first logs on. Normally a known folder is not created until it is first called. At that time, an API such as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder">SHCreateItemInKnownFolder</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getshellitem">IKnownFolder::GetShellItem</a> is called with the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KF_FLAG_CREATE</a> flag. However, some known folders need to exist immediately. An example is those known folders under %USERPROFILE%, which must exist to provide a proper view. In those cases, KFDF_PRECREATE is set and Windows Explorer calls the creation API during its user initialization.

### -field KFDF_STREAM:0x10

<b>Introduced in Windows 7</b>. The known folder is a file rather than a folder.

### -field KFDF_PUBLISHEXPANDEDPATH:0x20

<b>Introduced in Windows 7</b>. The full path of the known folder, with any environment variables fully expanded, is stored in the registry under HKEY_CURRENT_USER.

### -field KFDF_NO_REDIRECT_UI:0x40

<b>Introduced in Windows 8.1</b>. Prevent showing the <b>Locations</b> tab in the property dialog of the known folder. 

## -remarks

The <b>KF_DEFINITION_FLAGS</b> type is defined in Shobjidl.h as shown here.


```
typedef DWORD KF_DEFINITION_FLAGS;
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
