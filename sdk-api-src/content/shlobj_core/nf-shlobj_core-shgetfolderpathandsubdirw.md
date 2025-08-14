---
UID: NF:shlobj_core.SHGetFolderPathAndSubDirW
title: SHGetFolderPathAndSubDirW function (shlobj_core.h)
description: Gets the path of a folder and appends a user-provided subfolder path. (Unicode)
helpviewer_keywords: ["SHGFP_TYPE_CURRENT", "SHGFP_TYPE_DEFAULT", "SHGetFolderPathAndSubDir", "SHGetFolderPathAndSubDir function [Windows Shell]", "SHGetFolderPathAndSubDirW", "_shell_SHGetFolderPathAndSubDir", "shell.SHGetFolderPathAndSubDir", "shlobj_core/SHGetFolderPathAndSubDir", "shlobj_core/SHGetFolderPathAndSubDirW"]
old-location: shell\SHGetFolderPathAndSubDir.htm
tech.root: shell
ms.assetid: 7e92e136-1036-4c96-931f-6e0129fb839a
ms.date: 12/05/2018
ms.keywords: SHGFP_TYPE_CURRENT, SHGFP_TYPE_DEFAULT, SHGetFolderPathAndSubDir, SHGetFolderPathAndSubDir function [Windows Shell], SHGetFolderPathAndSubDirA, SHGetFolderPathAndSubDirW, _shell_SHGetFolderPathAndSubDir, shell.SHGetFolderPathAndSubDir, shlobj_core/SHGetFolderPathAndSubDir, shlobj_core/SHGetFolderPathAndSubDirA, shlobj_core/SHGetFolderPathAndSubDirW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetFolderPathAndSubDirW (Unicode) and SHGetFolderPathAndSubDirA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.60 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetFolderPathAndSubDirW
 - shlobj_core/SHGetFolderPathAndSubDirW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
api_name:
 - SHGetFolderPathAndSubDir
 - SHGetFolderPathAndSubDirA
 - SHGetFolderPathAndSubDirW
---

# SHGetFolderPathAndSubDirW function


## -description

Gets the path of a folder and appends a user-provided subfolder path.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

Reserved.

### -param csidl [in]

Type: <b>int</b>

A <a href="/windows/desktop/shell/csidl">CSIDL</a> value that identifies the folder whose path is to be retrieved. Only real folders are valid. If a virtual folder is specified, this function fails. You can force creation of a folder with <b>SHGetFolderPathAndSubDir</b> by combining the folder's <b>CSIDL</b> with CSIDL_FLAG_CREATE.

### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> that represents a particular user. For systems earlier than Windows 2000, set this value to <b>NULL</b>. For later systems, <i>hToken</i> is usually, but not always, set to <b>NULL</b>. You might need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <a href="/windows/desktop/shell/manage">My Documents</a>.

### -param dwFlags [in]

Type: <b>DWORD</b>

Specifies whether the path to be returned is the actual path of the folder or the default path. This value is used in cases where the folder associated with a <a href="/windows/desktop/shell/csidl">CSIDL</a> value may be moved or renamed by the user.



#### SHGFP_TYPE_CURRENT

Return the folder's current path.



#### SHGFP_TYPE_DEFAULT

Return the folder's default path.

### -param pszSubDir [in]

Type: <b>LPCTSTR</b>

A pointer to the subpath to be appended to the folder's path. This is a <b>null</b>-terminated string of length MAX_PATH. If you are not creating a new directory, this must be an existing subdirectory or the function returns an error. This value can be <b>NULL</b> if no subpath is to be appended.

### -param pszPath [out]

Type: <b>LPTSTR</b>

When this function returns, this value points to the directory path and appended subpath. This is a <b>null</b>-terminated string of length MAX_PATH. This string is empty when the function returns an error code.


##### - dwFlags.SHGFP_TYPE_CURRENT

Return the folder's current path.


##### - dwFlags.SHGFP_TYPE_DEFAULT

Return the folder's default path.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a>

## -remarks

> [!NOTE]
> The shlobj_core.h header defines SHGetFolderPathAndSubDir as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
