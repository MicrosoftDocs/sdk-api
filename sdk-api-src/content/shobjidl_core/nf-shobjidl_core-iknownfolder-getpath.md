---
UID: NF:shobjidl_core.IKnownFolder.GetPath
title: IKnownFolder::GetPath (shobjidl_core.h)
description: Retrieves the path of a known folder as a string.
helpviewer_keywords: ["GetPath","GetPath method [Windows Shell]","GetPath method [Windows Shell]","IKnownFolder interface","IKnownFolder interface [Windows Shell]","GetPath method","IKnownFolder.GetPath","IKnownFolder::GetPath","_shell_IKnownFolder_GetPath","shell.IKnownFolder_GetPath","shobjidl_core/IKnownFolder::GetPath"]
old-location: shell\IKnownFolder_GetPath.htm
tech.root: shell
ms.assetid: c1786db0-9bcc-4fc8-ae18-8519da6edda9
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [Windows Shell], GetPath method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetPath method, IKnownFolder.GetPath, IKnownFolder::GetPath, _shell_IKnownFolder_GetPath, shell.IKnownFolder_GetPath, shobjidl_core/IKnownFolder::GetPath
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
 - IKnownFolder::GetPath
 - shobjidl_core/IKnownFolder::GetPath
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
 - IKnownFolder.GetPath
---

# IKnownFolder::GetPath


## -description

Retrieves the path of a known folder as a string.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param ppszPath [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated buffer that contains the path. The calling application is responsible for calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free this resource when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Equivalent to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>