---
UID: NE:shlobj_core.KNOWN_FOLDER_FLAG
title: KNOWN_FOLDER_FLAG (shlobj_core.h)
description: Defines constants that specify special retrieval options for known folders. These values supersede CSIDL values, which have parallel meanings.
ms.date: 02/27/2023
helpviewer_keywords: ["KF_FLAG_ALIAS_ONLY","KF_FLAG_CREATE","KF_FLAG_DEFAULT","KF_FLAG_DEFAULT_PATH","KF_FLAG_DONT_UNEXPAND","KF_FLAG_DONT_VERIFY","KF_FLAG_FORCE_APPCONTAINER_REDIRECTION","KF_FLAG_FORCE_APP_DATA_REDIRECTION","KF_FLAG_FORCE_PACKAGE_REDIRECTION","KF_FLAG_INIT","KF_FLAG_NOT_PARENT_RELATIVE","KF_FLAG_NO_ALIAS","KF_FLAG_NO_APPCONTAINER_REDIRECTION","KF_FLAG_NO_PACKAGE_REDIRECTION","KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET","KF_FLAG_SIMPLE_IDLIST","KNOWN_FOLDER_FLAG","KNOWN_FOLDER_FLAG enumeration [Windows Shell]","_shell_KNOWN_FOLDER_FLAG","shell.KNOWN_FOLDER_FLAG","shlobj_core/KF_FLAG_ALIAS_ONLY","shlobj_core/KF_FLAG_CREATE","shlobj_core/KF_FLAG_DEFAULT","shlobj_core/KF_FLAG_DEFAULT_PATH","shlobj_core/KF_FLAG_DONT_UNEXPAND","shlobj_core/KF_FLAG_DONT_VERIFY","shlobj_core/KF_FLAG_FORCE_APPCONTAINER_REDIRECTION","shlobj_core/KF_FLAG_FORCE_APP_DATA_REDIRECTION","shlobj_core/KF_FLAG_FORCE_PACKAGE_REDIRECTION","shlobj_core/KF_FLAG_INIT","shlobj_core/KF_FLAG_NOT_PARENT_RELATIVE","shlobj_core/KF_FLAG_NO_ALIAS","shlobj_core/KF_FLAG_NO_APPCONTAINER_REDIRECTION","shlobj_core/KF_FLAG_NO_PACKAGE_REDIRECTION","shlobj_core/KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET","shlobj_core/KF_FLAG_SIMPLE_IDLIST","shlobj_core/KNOWN_FOLDER_FLAG"]
old-location: shell\KNOWN_FOLDER_FLAG.htm
tech.root: shell
ms.assetid: 7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KNOWN_FOLDER_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KNOWN_FOLDER_FLAG
 - shlobj_core/KNOWN_FOLDER_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - KNOWN_FOLDER_FLAG
---

# KNOWN_FOLDER_FLAG enumeration

## -description

Defines constants that specify special retrieval options for [known folders](/windows/win32/shell/known-folders) (for example, for use when calling the [SHGetKnownFolderIDList](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) function to retrieve the path of a known folder). These values supersede [CSIDL](/windows/win32/shell/csidl) values, which have parallel meanings.

## -enum-fields

### -field KF_FLAG_DEFAULT:0x00000000

Specifies no special retrieval options.

### -field KF_FLAG_FORCE_APP_DATA_REDIRECTION:0x00080000

**Introduced in Windows 10, version 1709**. When called from a packaged app, specifies that **LocalAppData**/**RoamingAppData** folders are redirected to private app locations that match the paths returned from [Windows.Storage.ApplicationData.Current](/uwp/api/windows.storage.applicationdata.current) in the **LocalFolder** and **RoamingFolder** properties. Other folders are redirected to subdirectories of **LocalAppData**.

This flag is used with **FOLDERID_AppDataDesktop**, **FOLDERID_AppDataDocuments**, **FOLDERID_AppDataFavorites**, and **FOLDERID_AppDataProgramData**. It's also intended for compatibility with .NET applications, and not meant to be used directly from an application.

### -field KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET:0x00040000

**Introduced in Windows 10, version 1703**. When running in a packaged process, specifies that some file system locations are redirected to package-specific locations by the file system. This flag causes the target of the direction to be returned for those locations. This is useful in cases where the real location within the file system needs to be known.

### -field KF_FLAG_FORCE_PACKAGE_REDIRECTION:0x00020000

**Introduced in Windows 10, version 1703**. When running inside an AppContainer process, or when providing an AppContainer token, specifies that some folders are redirected to AppContainer-specific locations within the package. This flag forces redirection (for folders that aren't normally redirected) for the purposes of packaged processes, and can be used for sharing files between UWP and packaged apps within the same package. This flag supersedes the deprecated **KF_FLAG_FORCE_APPCONTAINER_REDIRECTION**.

### -field KF_FLAG_NO_PACKAGE_REDIRECTION:0x00010000

**Introduced in Windows 10, version 1703**. When running inside a packaged process, or when providing a packaged process token, specifies that some folders are redirected to package-specific locations. This flag disables redirection on locations where it's applied, and instead returns the path that would be returned were it not running inside a packaged process. This flag supersedes the deprecated **KF_FLAG_NO_APPCONTAINER_REDIRECTION**.

### -field KF_FLAG_FORCE_APPCONTAINER_REDIRECTION:0x00020000

**Introduced in Windows 8**. This flag was deprecated in Windows 10, version 1703. Use **KF_FLAG_FORCE_PACKAGE_REDIRECTION** instead.

### -field KF_FLAG_NO_APPCONTAINER_REDIRECTION:0x00010000

**Introduced in Windows 8**. This flag was deprecated in Windows 10, version 1703. Use **KF_FLAG_NO_PACKAGE_REDIRECTION** instead.

### -field KF_FLAG_CREATE:0x00008000

Specifies to force the creation of the specified folder if that folder doesn't already exist. The security provisions predefined for that folder are applied. If the folder doesn't exist and can't be created, then the function returns a failure code, and no path is returned. This value can be used only with the following functions and methods:

* [SHGetKnownFolderPath](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
* [SHGetKnownFolderIDList](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)
* [IKnownFolder::GetIDList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist)
* [IKnownFolder::GetPath](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)
* [IKnownFolder::GetShellItem](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getshellitem)

### -field KF_FLAG_DONT_VERIFY:0x00004000

Specifies not to verify the folder's existence before attempting to retrieve the path or IDList. If this flag isn't set, then an attempt is made to verify that the folder is truly present at the path. If that verification fails due to the folder being absent or inaccessible, then the function returns a failure code, and no path is returned.

If the folder is located on a network, then the function might take longer to execute. So setting this flag can reduce that latency.

### -field KF_FLAG_DONT_UNEXPAND:0x00002000

Specfies to store the full path in the registry without using environment strings. If this flag isn't set, then portions of the path might be represented by environment strings such as `%USERPROFILE%`. This flag can be used only with [SHSetKnownFolderPath](/windows/win32/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath) and [IKnownFolder::SetPath](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath).

### -field KF_FLAG_NO_ALIAS:0x00001000

Specifies to retrieve the true system path for the folder, free of any aliased placeholders such as `%USERPROFILE%`, returned by [SHGetKnownFolderIDList](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) and [IKnownFolder::GetIDList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist). This flag has no effect on paths returned by [SHGetKnownFolderPath](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) and [IKnownFolder::GetPath](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath). By default, known folder retrieval functions and methods return the aliased path if an alias exists.

### -field KF_FLAG_INIT:0x00000800

Specifies to initialize the folder using its `Desktop.ini` settings. If the folder can't be initialized, then the function returns a failure code, and no path is returned. This flag should always be combined with **KF_FLAG_CREATE**.

If the folder is located on a network, then the function might take longer to execute.

### -field KF_FLAG_DEFAULT_PATH:0x00000400

Specifies to retrieve the default path for a known folder. If this flag isn't set, then the function retrieves the current&mdash;and possibly redirected&mdash;path of the folder. The execution of this flag includes a verification of the folder's existence unless **KF_FLAG_DONT_VERIFY** is set.

### -field KF_FLAG_NOT_PARENT_RELATIVE:0x00000200

Specifies to retrieve the folder's default path independent of the current location of its parent. **KF_FLAG_DEFAULT_PATH** must also be set.

### -field KF_FLAG_SIMPLE_IDLIST:0x00000100

Specifies to build a simple IDList (PIDL). This value can be used when you want to retrieve the file system path. But don't specify this value if you're retrieving the localized display name of the folder, because it might not resolve correctly.

### -field KF_FLAG_ALIAS_ONLY:0x80000000

**Introduced in Windows 7**. Specifies to retrieve only aliased PIDLs. Don't use the file system path.

## -remarks

These values, with the exception of **KF_FLAG_ALIAS_ONLY**, were defined in Windows Vista as individual constants. They're defined as an enumeration only in Windows 7 and later. However, all underlying numerical values are the same in either form.

## -see-also

* [IKnownFolder::GetShellItem](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getshellitem)
* [Known folders sample app](/windows/win32/shell/samples-knownfolders)
