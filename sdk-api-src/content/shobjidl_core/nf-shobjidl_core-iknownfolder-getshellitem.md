---
UID: NF:shobjidl_core.IKnownFolder.GetShellItem
title: IKnownFolder::GetShellItem (shobjidl_core.h)
description: Retrieves the location of a known folder in the Shell namespace in the form of a Shell item (IShellItem or derived interface).
helpviewer_keywords: ["GetShellItem","GetShellItem method [Windows Shell]","GetShellItem method [Windows Shell]","IKnownFolder interface","IKnownFolder interface [Windows Shell]","GetShellItem method","IKnownFolder.GetShellItem","IKnownFolder::GetShellItem","_shell_IKnownFolder_GetShellItem","shell.IKnownFolder_GetShellItem","shobjidl_core/IKnownFolder::GetShellItem"]
old-location: shell\IKnownFolder_GetShellItem.htm
tech.root: shell
ms.assetid: a42c0a20-9c72-48d3-8432-15b73ff211d2
ms.date: 12/05/2018
ms.keywords: GetShellItem, GetShellItem method [Windows Shell], GetShellItem method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetShellItem method, IKnownFolder.GetShellItem, IKnownFolder::GetShellItem, _shell_IKnownFolder_GetShellItem, shell.IKnownFolder_GetShellItem, shobjidl_core/IKnownFolder::GetShellItem
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
 - IKnownFolder::GetShellItem
 - shobjidl_core/IKnownFolder::GetShellItem
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
 - IKnownFolder.GetShellItem
---

# IKnownFolder::GetShellItem


## -description

Retrieves the location of a known folder in the Shell namespace in the form of a Shell item (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or derived interface).

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param riid

Type: <b>REFIID</b>

A reference to the IID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>