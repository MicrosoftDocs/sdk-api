---
UID: NS:shobjidl_core.KNOWNFOLDER_DEFINITION
title: KNOWNFOLDER_DEFINITION (shobjidl_core.h)
description: Defines the specifics of a known folder.
helpviewer_keywords: ["KNOWNFOLDER_DEFINITION","KNOWNFOLDER_DEFINITION structure [Windows Shell]","_shell_KNOWNFOLDER_DEFINITION","shell.KNOWNFOLDER_DEFINITION","shobjidl_core/KNOWNFOLDER_DEFINITION"]
old-location: shell\KNOWNFOLDER_DEFINITION.htm
tech.root: shell
ms.assetid: 08bd8406-68fa-4e02-9a64-ed5e62f8639b
ms.date: 12/05/2018
ms.keywords: KNOWNFOLDER_DEFINITION, KNOWNFOLDER_DEFINITION structure [Windows Shell], _shell_KNOWNFOLDER_DEFINITION, shell.KNOWNFOLDER_DEFINITION, shobjidl_core/KNOWNFOLDER_DEFINITION
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
req.typenames: KNOWNFOLDER_DEFINITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KNOWNFOLDER_DEFINITION
 - shobjidl_core/KNOWNFOLDER_DEFINITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - KNOWNFOLDER_DEFINITION
---

# KNOWNFOLDER_DEFINITION structure


## -description

Defines the specifics of a known folder.

## -struct-fields

### -field category

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY</a></b>

A single value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY</a> constants that classifies the folder as virtual, fixed, common, or per-user.

### -field pszName

Type: <b>LPWSTR</b>

A pointer to the non-localized, canonical name for the known folder, stored as a null-terminated Unicode string. If this folder is a common or per-user folder, this value is also used as the value name of the "User Shell Folders" registry settings. This name is meant to be a unique, human-readable name. Third parties are recommended to follow the format <code>Company.Application.Name</code>. The name given here should not be confused with the display name.

### -field pszDescription

Type: <b>LPWSTR</b>

A pointer to a short description of the known folder, stored as a null-terminated Unicode string. This description should include the folder's purpose and usage.

### -field fidParent

Type: <b><a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a></b>

A <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> value that names another known folder to serve as the parent folder. Applies to common and per-user folders only. This value is used in conjunction with <b>pszRelativePath</b>. See <b>Remarks</b> for more details.
                        
                        

This value is optional if no value is provided for <b>pszRelativePath</b>.

### -field pszRelativePath

Type: <b>LPWSTR</b>

Optional. A pointer to a path relative to the parent folder specified in <b>fidParent</b>. This is a null-terminated Unicode string, refers to the physical file system path, and is not localized. Applies to common and per-user folders only. See <b>Remarks</b> for more details.

### -field pszParsingName

Type: <b>LPWSTR</b>

A pointer to the Shell namespace folder path of the folder, stored as a null-terminated Unicode string. Applies to virtual folders only. For example, <code>Control Panel</code> has a parsing name of <code>::%CLSID_MyComputer%\::%CLSID_ControlPanel%</code>.

### -field pszTooltip

Type: <b>LPWSTR</b>

Optional. A pointer to the default tooltip resource used for this known folder when it is created. This is a null-terminated Unicode string in this form:
    
                        

<b>Module name, Resource ID</b>

For example, <code>@%_SYS_MOD_PATH%,-12688</code> is the tooltip for Common Pictures. When the folder is created, this string is stored in that folder's copy of Desktop.ini. It can be changed later by other Shell APIs. This resource might be localized.

This information is not required for virtual folders.

### -field pszLocalizedName

Type: <b>LPWSTR</b>

Optional. A pointer to the default localized name resource used when the folder is created. This is a null-terminated Unicode string in this form:
    
                        

<b>Module name, Resource ID</b>

When the folder is created, this string is stored in that folder's copy of Desktop.ini. It can be changed later by other Shell APIs.

This information is not required for virtual folders.

### -field pszIcon

Type: <b>LPWSTR</b>

Optional. A pointer to the default icon resource used when the folder is created. This is a null-terminated Unicode string in this form:
    
                        

<b>Module name, Resource ID</b>

When the folder is created, this string is stored in that folder's copy of Desktop.ini. It can be changed later by other Shell APIs.

This information is not required for virtual folders.

### -field pszSecurity

Type: <b>LPWSTR</b>

Optional. A pointer to a <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> format string. This is a null-terminated Unicode string that describes the default security descriptor that the folder receives when it is created. If this parameter is <b>NULL</b>, the new folder inherits the security descriptor of its parent. This is particularly useful for common folders that are accessed by all users.

### -field dwAttributes

Type: <b>DWORD</b>

Optional. Default file system attributes given to the folder when it is created. For example, the file could be hidden and read-only (FILE_ATTRIBUTE_HIDDEN and FILE_ATTRIBUTE_READONLY). For a complete list of possible values, see the <i>dwFlagsAndAttributes</i> parameter of the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. Set to -1 if not needed.

### -field kfdFlags

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags">KF_DEFINITION_FLAGS</a></b>

Optional. One of more values from the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags">KF_DEFINITION_FLAGS</a> enumeration that allow you to restrict redirection, allow PC-to-PC roaming, and control the time at which the known folder is created. Set to 0 if not needed.

### -field ftidType

Type: <b><a href="/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a></b>

One of the <a href="/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a> values that identifies the known folder type based on its contents (such as documents, music, or photographs). This value is a GUID.

## -remarks

The <b>fidParent</b> and <b>pszRelativePath</b> values work together. For example, suppose you are defining a folder called MyNewFolder and want to create that folder as ...\&lt;Username&gt;\AppData\Local\MyApp\MyNewFolder. Provide <a href="/windows/desktop/shell/knownfolderid">FOLDERID_LocalAppData</a> in <b>fidParent</b> to represent ...\&lt;Username&gt;\AppData\Local. Provide "\MyApp\MyNewFolder" in <b>pszRelativePath</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition">IKnownFolder::GetFolderDefinition</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder">IKnownFolderManager::RegisterFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>