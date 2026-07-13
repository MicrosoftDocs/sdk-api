---
UID: NF:shobjidl_core.IKnownFolder.SetPath
title: IKnownFolder::SetPath (shobjidl_core.h)
description: Assigns a new path to a known folder.
helpviewer_keywords: ["IKnownFolder interface [Windows Shell]","SetPath method","IKnownFolder.SetPath","IKnownFolder::SetPath","KF_FLAG_DONT_UNEXPAND","SetPath","SetPath method [Windows Shell]","SetPath method [Windows Shell]","IKnownFolder interface","_shell_IKnownFolder_SetPath","shell.IKnownFolder_SetPath","shobjidl_core/IKnownFolder::SetPath"]
old-location: shell\IKnownFolder_SetPath.htm
tech.root: shell
ms.assetid: 235f69de-3571-4184-aa52-b409fbc1d643
ms.date: 12/05/2018
ms.keywords: IKnownFolder interface [Windows Shell],SetPath method, IKnownFolder.SetPath, IKnownFolder::SetPath, KF_FLAG_DONT_UNEXPAND, SetPath, SetPath method [Windows Shell], SetPath method [Windows Shell],IKnownFolder interface, _shell_IKnownFolder_SetPath, shell.IKnownFolder_SetPath, shobjidl_core/IKnownFolder::SetPath
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnownFolder::SetPath
 - shobjidl_core/IKnownFolder::SetPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder.SetPath
---

# IKnownFolder::SetPath


## -description

Assigns a new path to a known folder.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Either zero or the following value:



#### KF_FLAG_DONT_UNEXPAND

Set the full path without environment strings. If this flag is not set, portions of the path at <i>pszPath</i> may be represented by environment strings such as <code>%USERPROFILE%</code>.

### -param pszPath [in]

Type: <b>LPCWSTR</b>

Pointer to the folder's new path. This is a null-terminated Unicode string of length MAX_PATH. This path cannot be of zero length. If this value is <b>NULL</b>, the <b>IKnownFolder::SetPath</b> sets the path to the default value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method cannot be called on folders of type <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_FIXED</a> or <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_VIRTUAL</a>.

To call this method on a folder of type <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_COMMON</a>, the calling application must be running with elevated privileges.

This method is equivalent to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a>