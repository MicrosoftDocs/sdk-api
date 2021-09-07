---
UID: NF:shobjidl_core.ICommDlgBrowser2.GetViewFlags
title: ICommDlgBrowser2::GetViewFlags (shobjidl_core.h)
description: Called when the view must determine if special customization needs to be made for the common dialog browser.
helpviewer_keywords: ["CDB2GVF_ADDSHIELD","CDB2GVF_ALLOWPREVIEWPANE","CDB2GVF_ISFILESAVE","CDB2GVF_ISFOLDERPICKER","CDB2GVF_NOINCLUDEITEM","CDB2GVF_NOSELECTVERB","CDB2GVF_SHOWALLFILES","GetViewFlags","GetViewFlags method [Windows Shell]","GetViewFlags method [Windows Shell]","ICommDlgBrowser2 interface","ICommDlgBrowser2 interface [Windows Shell]","GetViewFlags method","ICommDlgBrowser2.GetViewFlags","ICommDlgBrowser2::GetViewFlags","_win32_ICommDlgBrowser2_GetViewFlags","shell.ICommDlgBrowser2_GetViewFlags","shobjidl_core/ICommDlgBrowser2::GetViewFlags"]
old-location: shell\ICommDlgBrowser2_GetViewFlags.htm
tech.root: shell
ms.assetid: cb22504c-9f76-44c4-b81d-fc15d1b95143
ms.date: 12/05/2018
ms.keywords: CDB2GVF_ADDSHIELD, CDB2GVF_ALLOWPREVIEWPANE, CDB2GVF_ISFILESAVE, CDB2GVF_ISFOLDERPICKER, CDB2GVF_NOINCLUDEITEM, CDB2GVF_NOSELECTVERB, CDB2GVF_SHOWALLFILES, GetViewFlags, GetViewFlags method [Windows Shell], GetViewFlags method [Windows Shell],ICommDlgBrowser2 interface, ICommDlgBrowser2 interface [Windows Shell],GetViewFlags method, ICommDlgBrowser2.GetViewFlags, ICommDlgBrowser2::GetViewFlags, _win32_ICommDlgBrowser2_GetViewFlags, shell.ICommDlgBrowser2_GetViewFlags, shobjidl_core/ICommDlgBrowser2::GetViewFlags
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
 - ICommDlgBrowser2::GetViewFlags
 - shobjidl_core/ICommDlgBrowser2::GetViewFlags
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
 - ICommDlgBrowser2.GetViewFlags
---

# ICommDlgBrowser2::GetViewFlags


## -description

Called when the view must determine if special customization needs to be made for the common dialog browser.

## -parameters

### -param pdwFlags

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that controls the behavior of the view when in common dialog mode.



#### CDB2GVF_SHOWALLFILES (0x00000001)

0x00000001. All files, including hidden and system files, should be shown. In Windows XP, this is the only recognized flag.



#### CDB2GVF_ISFILESAVE (0x00000002)

0x00000002. This browser is designated to choose a file to save.



#### CDB2GVF_ALLOWPREVIEWPANE (0x00000004)

0x00000004. Not used.



#### CDB2GVF_NOSELECTVERB (0x00000008)

0x00000008. Do not show a "<code>select</code>" verb on an item's context menu.



#### CDB2GVF_NOINCLUDEITEM (0x00000010)

0x00000010. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icommdlgbrowser-includeobject">IncludeObject</a> should not be called.



#### CDB2GVF_ISFOLDERPICKER (0x00000020)

0x00000020. This browser is designated to pick folders.



#### CDB2GVF_ADDSHIELD (0x00000040)

0x00000040. <b>Windows 7 and later</b>. Displays a UAC shield on the selected item when CDB2GVF_NOSELECTVERB is not specified.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>