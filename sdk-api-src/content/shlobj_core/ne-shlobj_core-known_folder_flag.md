---
UID: NE:shlobj_core.__unnamed_enum_3
title: KNOWN_FOLDER_FLAG (shlobj_core.h)
description: Specify special retrieval options for known folders. These values supersede CSIDL values, which have parallel meanings.
helpviewer_keywords: ["KF_FLAG_ALIAS_ONLY","KF_FLAG_CREATE","KF_FLAG_DEFAULT","KF_FLAG_DEFAULT_PATH","KF_FLAG_DONT_UNEXPAND","KF_FLAG_DONT_VERIFY","KF_FLAG_FORCE_APPCONTAINER_REDIRECTION","KF_FLAG_FORCE_APP_DATA_REDIRECTION","KF_FLAG_FORCE_PACKAGE_REDIRECTION","KF_FLAG_INIT","KF_FLAG_NOT_PARENT_RELATIVE","KF_FLAG_NO_ALIAS","KF_FLAG_NO_APPCONTAINER_REDIRECTION","KF_FLAG_NO_PACKAGE_REDIRECTION","KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET","KF_FLAG_SIMPLE_IDLIST","KNOWN_FOLDER_FLAG","KNOWN_FOLDER_FLAG enumeration [Windows Shell]","_shell_KNOWN_FOLDER_FLAG","shell.KNOWN_FOLDER_FLAG","shlobj_core/KF_FLAG_ALIAS_ONLY","shlobj_core/KF_FLAG_CREATE","shlobj_core/KF_FLAG_DEFAULT","shlobj_core/KF_FLAG_DEFAULT_PATH","shlobj_core/KF_FLAG_DONT_UNEXPAND","shlobj_core/KF_FLAG_DONT_VERIFY","shlobj_core/KF_FLAG_FORCE_APPCONTAINER_REDIRECTION","shlobj_core/KF_FLAG_FORCE_APP_DATA_REDIRECTION","shlobj_core/KF_FLAG_FORCE_PACKAGE_REDIRECTION","shlobj_core/KF_FLAG_INIT","shlobj_core/KF_FLAG_NOT_PARENT_RELATIVE","shlobj_core/KF_FLAG_NO_ALIAS","shlobj_core/KF_FLAG_NO_APPCONTAINER_REDIRECTION","shlobj_core/KF_FLAG_NO_PACKAGE_REDIRECTION","shlobj_core/KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET","shlobj_core/KF_FLAG_SIMPLE_IDLIST","shlobj_core/KNOWN_FOLDER_FLAG"]
old-location: shell\KNOWN_FOLDER_FLAG.htm
tech.root: shell
ms.assetid: 7f99fb6c-32f2-4fd8-ad11-3ad84d17c5c1
ms.date: 12/05/2018
ms.keywords: KF_FLAG_ALIAS_ONLY, KF_FLAG_CREATE, KF_FLAG_DEFAULT, KF_FLAG_DEFAULT_PATH, KF_FLAG_DONT_UNEXPAND, KF_FLAG_DONT_VERIFY, KF_FLAG_FORCE_APPCONTAINER_REDIRECTION, KF_FLAG_FORCE_APP_DATA_REDIRECTION, KF_FLAG_FORCE_PACKAGE_REDIRECTION, KF_FLAG_INIT, KF_FLAG_NOT_PARENT_RELATIVE, KF_FLAG_NO_ALIAS, KF_FLAG_NO_APPCONTAINER_REDIRECTION, KF_FLAG_NO_PACKAGE_REDIRECTION, KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET, KF_FLAG_SIMPLE_IDLIST, KNOWN_FOLDER_FLAG, KNOWN_FOLDER_FLAG enumeration [Windows Shell], _shell_KNOWN_FOLDER_FLAG, shell.KNOWN_FOLDER_FLAG, shlobj_core/KF_FLAG_ALIAS_ONLY, shlobj_core/KF_FLAG_CREATE, shlobj_core/KF_FLAG_DEFAULT, shlobj_core/KF_FLAG_DEFAULT_PATH, shlobj_core/KF_FLAG_DONT_UNEXPAND, shlobj_core/KF_FLAG_DONT_VERIFY, shlobj_core/KF_FLAG_FORCE_APPCONTAINER_REDIRECTION, shlobj_core/KF_FLAG_FORCE_APP_DATA_REDIRECTION, shlobj_core/KF_FLAG_FORCE_PACKAGE_REDIRECTION, shlobj_core/KF_FLAG_INIT, shlobj_core/KF_FLAG_NOT_PARENT_RELATIVE, shlobj_core/KF_FLAG_NO_ALIAS, shlobj_core/KF_FLAG_NO_APPCONTAINER_REDIRECTION, shlobj_core/KF_FLAG_NO_PACKAGE_REDIRECTION, shlobj_core/KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET, shlobj_core/KF_FLAG_SIMPLE_IDLIST, shlobj_core/KNOWN_FOLDER_FLAG
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

Specify special retrieval options for known folders. These values supersede <a href="/windows/desktop/shell/csidl">CSIDL</a> values, which have parallel meanings.

## -enum-fields

### -field KF_FLAG_DEFAULT:0x00000000

0x00000000. No flags.

### -field KF_FLAG_FORCE_APP_DATA_REDIRECTION:0x00080000

0x00080000. Introduced in Windows 10, version 1709. When called from a packaged app, <b>LocalAppData/RoamingAppData</b> folders are redirected to private app locations that match the paths returned from <a href="/uwp/api/Windows.Storage.ApplicationData">Windows.Storage.ApplicationData.Current{LocalFolder|RoamingFolder}</a>. Other folders are redirected to subdirectories of <b>LocalAppData</b>

This flag is used with <b>FOLDERID_AppDataDesktop</b>, <b>FOLDERID_AppDataDocuments</b>, <b>FOLDERID_AppDataFavorites</b>, and <b>FOLDERID_AppDataProgramData</b>. It is also intended for compatibility with .NET applications, and not meant to be used directly from an application.

### -field KF_FLAG_RETURN_FILTER_REDIRECTION_TARGET:0x00040000

0x00040000. <b>Introduced in Windows 10, version 1703</b>. When running in a Desktop Bridge process, some file system locations are redirected to package-specific locations by the file system. This flag will cause the target of the direction to be returned for those locations. This is useful in cases where the real location within the file system needs to be known.

### -field KF_FLAG_FORCE_PACKAGE_REDIRECTION:0x00020000

0x00020000. <b>Introduced in Windows 10, version 1703</b>. When running inside an AppContainer process, or when providing an AppContainer token, some folders are redirected to AppContainer-specific locations within the package. This flag will force with redirection for folders that are not normally redirected for the purposes of Desktop Bridge processes, and can be used for sharing files between UWA and Desktop Bridge apps within the same package. This flag is functionally identical to <b>KF_FLAG_FORCE_APPCONTAINER_REDIRECTION</b>.

### -field KF_FLAG_NO_PACKAGE_REDIRECTION:0x00010000

0x00010000. <b>Introduced in Windows 10, version 1703</b>. When running inside a packaged process (such as a Desktop Bridge app or an AppContainer), or when providing a packaged process token, some folders are redirected to package-specific locations. This flag disables redirection on locations where it is applied, and instead returns the path that would be returned were it not running inside a packaged process. This flag is functionally identical to <b>KF_FLAG_NO_APPCONTAINER_REDIRECTION</b>.

### -field KF_FLAG_FORCE_APPCONTAINER_REDIRECTION:0x00020000

0x00020000. Introduced in Windows 8. This flag is functionally identical to <b>KF_FLAG_FORCE_PACKAGE_REDIRECTION</b>, and was deprecated in Windows 10, version 1703.

### -field KF_FLAG_NO_APPCONTAINER_REDIRECTION:0x00010000

0x00010000. <b>Introduced in Windows 8</b>. This flag is functionally identical to <b>KF_FLAG_NO_PACKAGE_REDIRECTION</b> and was deprecated in Windows 10, version 1703.

### -field KF_FLAG_CREATE:0x00008000

0x00008000. Forces the creation of the specified folder if that folder does not already exist. The security provisions predefined for that folder are applied. If the folder does not exist and cannot be created, the function returns a failure code and no path is returned. This value can be used only with the following functions and methods:
                        
                        

<ul>
<li>
<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>
</li>
<li>
<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist">IKnownFolder::GetIDList</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">IKnownFolder::GetPath</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getshellitem">IKnownFolder::GetShellItem</a>
</li>
</ul>

### -field KF_FLAG_DONT_VERIFY:0x00004000

0x00004000. Do not verify the folder's existence before attempting to retrieve the path or IDList. If this flag is not set, an attempt is made to verify that the folder is truly present at the path. If that verification fails due to the folder being absent or inaccessible, the function returns a failure code and no path is returned.
              
                        

If the folder is located on a network, the function might take a longer time to execute. Setting this flag can reduce that lag time.

### -field KF_FLAG_DONT_UNEXPAND:0x00002000

0x00002000. Stores the full path in the registry without using environment strings. If this flag is not set, portions of the path may be represented by environment strings such as %USERPROFILE%. This flag can only be used with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath">IKnownFolder::SetPath</a>.

### -field KF_FLAG_NO_ALIAS:0x00001000

0x00001000. Gets the true system path for the folder, free of any aliased placeholders such as %USERPROFILE%, returned by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist">IKnownFolder::GetIDList</a>. This flag has no effect on paths returned by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">IKnownFolder::GetPath</a>. By default, known folder retrieval functions and methods return the aliased path if an alias exists.

### -field KF_FLAG_INIT:0x00000800

0x00000800. Initializes the folder using its Desktop.ini settings. If the folder cannot be initialized, the function returns a failure code and no path is returned. This flag should always be combined with KF_FLAG_CREATE.
        
            			

If the folder is located on a network, the function might take a longer time to execute.

### -field KF_FLAG_DEFAULT_PATH:0x00000400

0x00000400. Gets the default path for a known folder. If this flag is not set, the function retrieves the current—and possibly redirected—path of the folder. The execution of this flag includes a verification of the folder's existence unless KF_FLAG_DONT_VERIFY is set.

### -field KF_FLAG_NOT_PARENT_RELATIVE:0x00000200

0x00000200. Gets the folder's default path independent of the current location of its parent. KF_FLAG_DEFAULT_PATH must also be set.

### -field KF_FLAG_SIMPLE_IDLIST:0x00000100

0x00000100. Build a simple IDList (PIDL) This value can be used when you want to retrieve the file system path but do not specify this value if you are retrieving the localized display name of the folder because it might not resolve correctly.

### -field KF_FLAG_ALIAS_ONLY:0x80000000

0x80000000. <b>Introduced in Windows 7</b>. Return only aliased PIDLs. Do not use the file system path.

## -remarks

These values, with the exception of KF_FLAG_ALIAS_ONLY, were defined in Windows Vista as individual constants. They are defined as an enumeration only in Windows 7 and later. However, all underlying numerical values are the same in either form.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getshellitem">IKnownFolder::GetShellItem</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder">SHCreateItemInKnownFolder</a>
