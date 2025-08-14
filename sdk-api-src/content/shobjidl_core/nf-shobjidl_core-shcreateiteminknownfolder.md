---
UID: NF:shobjidl_core.SHCreateItemInKnownFolder
title: SHCreateItemInKnownFolder function (shobjidl_core.h)
description: Creates a Shell item object for a single file that exists inside a known folder.
helpviewer_keywords: ["SHCreateItemInKnownFolder","SHCreateItemInKnownFolder function [Windows Shell]","_shell_SHCreateItemInKnownFolder","shell.SHCreateItemInKnownFolder","shobjidl_core/SHCreateItemInKnownFolder"]
old-location: shell\SHCreateItemInKnownFolder.htm
tech.root: shell
ms.assetid: dc75ee60-7319-4a11-949e-dd0c3deabd8f
ms.date: 12/05/2018
ms.keywords: SHCreateItemInKnownFolder, SHCreateItemInKnownFolder function [Windows Shell], _shell_SHCreateItemInKnownFolder, shell.SHCreateItemInKnownFolder, shobjidl_core/SHCreateItemInKnownFolder
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateItemInKnownFolder
 - shobjidl_core/SHCreateItemInKnownFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - SHCreateItemInKnownFolder
req.apiset: ext-ms-win-shell-shell32-l1-2-0 (introduced in Windows 8.1)
---

# SHCreateItemInKnownFolder function


## -description

Creates a Shell item object for a single file that exists inside a known folder.

## -parameters

### -param kfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>, a <b>GUID</b> that identifies the folder that contains the item.

### -param dwKFFlags

Type: <b>DWORD</b>

Flags that specify special options in the object retrieval. This value can be 0; otherwise, one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param pszItem [in, optional]

Type: <b>PCWSTR</b>

A pointer to a null-terminated buffer that contains the file name of the new item as a Unicode string. This parameter can also be <b>NULL</b>. In this case, an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the known folder itself is created.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface that represents the item, retrieved through <i>ppv</i>. This value is typically IID_IShellItem or IID_IShellItem2.

### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
