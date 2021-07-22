---
UID: NF:shobjidl_core.IKnownFolder.GetIDList
title: IKnownFolder::GetIDList (shobjidl_core.h)
description: Gets the location of the Shell namespace folder in the IDList (ITEMIDLIST) form.
helpviewer_keywords: ["GetIDList","GetIDList method [Windows Shell]","GetIDList method [Windows Shell]","IKnownFolder interface","IKnownFolder interface [Windows Shell]","GetIDList method","IKnownFolder.GetIDList","IKnownFolder::GetIDList","_shell_IKnownFolder_GetIDList","shell.IKnownFolder_GetIDList","shobjidl_core/IKnownFolder::GetIDList"]
old-location: shell\IKnownFolder_GetIDList.htm
tech.root: shell
ms.assetid: b1c77198-da52-4f74-9e20-56b6d1d450f5
ms.date: 12/05/2018
ms.keywords: GetIDList, GetIDList method [Windows Shell], GetIDList method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetIDList method, IKnownFolder.GetIDList, IKnownFolder::GetIDList, _shell_IKnownFolder_GetIDList, shell.IKnownFolder_GetIDList, shobjidl_core/IKnownFolder::GetIDList
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
 - IKnownFolder::GetIDList
 - shobjidl_core/IKnownFolder::GetIDList
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
 - IKnownFolder.GetIDList
---

# IKnownFolder::GetIDList


## -description

Gets the location of the Shell namespace folder in the IDList (<a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>) form.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of an absolute PIDL. This parameter is passed uninitialized. The calling application is responsible for freeing this resource when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Equivalent to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>