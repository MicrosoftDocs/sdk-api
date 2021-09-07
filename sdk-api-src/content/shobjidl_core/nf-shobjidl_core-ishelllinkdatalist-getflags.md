---
UID: NF:shobjidl_core.IShellLinkDataList.GetFlags
title: IShellLinkDataList::GetFlags (shobjidl_core.h)
description: Gets the current option settings.
helpviewer_keywords: ["GetFlags","GetFlags method [Windows Shell]","GetFlags method [Windows Shell]","IShellLinkDataList interface","IShellLinkDataList interface [Windows Shell]","GetFlags method","IShellLinkDataList.GetFlags","IShellLinkDataList::GetFlags","_win32_IShellLinkDataList_GetFlags","shell.IShellLinkDataList_GetFlags","shobjidl_core/IShellLinkDataList::GetFlags"]
old-location: shell\IShellLinkDataList_GetFlags.htm
tech.root: shell
ms.assetid: d6ebfd84-6ef4-43be-af16-71fc395c4735
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Windows Shell], GetFlags method [Windows Shell],IShellLinkDataList interface, IShellLinkDataList interface [Windows Shell],GetFlags method, IShellLinkDataList.GetFlags, IShellLinkDataList::GetFlags, _win32_IShellLinkDataList_GetFlags, shell.IShellLinkDataList_GetFlags, shobjidl_core/IShellLinkDataList::GetFlags
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
 - IShellLinkDataList::GetFlags
 - shobjidl_core/IShellLinkDataList::GetFlags
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
 - IShellLinkDataList.GetFlags
---

# IShellLinkDataList::GetFlags


## -description

Gets the current option settings.

## -parameters

### -param pdwFlags [out]

Type: <b>DWORD*</b>

Pointer to one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags">SHELL_LINK_DATA_FLAGS</a> that indicate the current option settings.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>