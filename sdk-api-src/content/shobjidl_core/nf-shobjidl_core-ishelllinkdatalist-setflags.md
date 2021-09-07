---
UID: NF:shobjidl_core.IShellLinkDataList.SetFlags
title: IShellLinkDataList::SetFlags (shobjidl_core.h)
description: Sets the current option settings.
helpviewer_keywords: ["IShellLinkDataList interface [Windows Shell]","SetFlags method","IShellLinkDataList.SetFlags","IShellLinkDataList::SetFlags","SetFlags","SetFlags method [Windows Shell]","SetFlags method [Windows Shell]","IShellLinkDataList interface","_win32_IShellLinkDataList_SetFlags","shell.IShellLinkDataList_SetFlags","shobjidl_core/IShellLinkDataList::SetFlags"]
old-location: shell\IShellLinkDataList_SetFlags.htm
tech.root: shell
ms.assetid: 0fca6394-e8ad-4ef3-a7d8-60e85229556b
ms.date: 12/05/2018
ms.keywords: IShellLinkDataList interface [Windows Shell],SetFlags method, IShellLinkDataList.SetFlags, IShellLinkDataList::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IShellLinkDataList interface, _win32_IShellLinkDataList_SetFlags, shell.IShellLinkDataList_SetFlags, shobjidl_core/IShellLinkDataList::SetFlags
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkDataList::SetFlags
 - shobjidl_core/IShellLinkDataList::SetFlags
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
 - IShellLinkDataList.SetFlags
---

# IShellLinkDataList::SetFlags


## -description

Sets the current option settings.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

One or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags">SHELL_LINK_DATA_FLAGS</a> that indicate the option settings.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>