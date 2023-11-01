---
UID: NF:shobjidl_core.ICommDlgBrowser2.Notify
title: ICommDlgBrowser2::Notify (shobjidl_core.h)
description: Called by a Shell view to notify the common dialog box hosting it that an event has occurred.
helpviewer_keywords: ["CDB2N_CONTEXTMENU_DONE","CDB2N_CONTEXTMENU_START","ICommDlgBrowser2 interface [Windows Shell]","Notify method","ICommDlgBrowser2.Notify","ICommDlgBrowser2::Notify","Notify","Notify method [Windows Shell]","Notify method [Windows Shell]","ICommDlgBrowser2 interface","_win32_ICommDlgBrowser2_Notify","shell.ICommDlgBrowser2_Notify","shobjidl_core/ICommDlgBrowser2::Notify"]
old-location: shell\ICommDlgBrowser2_Notify.htm
tech.root: shell
ms.assetid: 486c306d-90ea-4ea4-afe1-2c3f5015ccf7
ms.date: 12/05/2018
ms.keywords: CDB2N_CONTEXTMENU_DONE, CDB2N_CONTEXTMENU_START, ICommDlgBrowser2 interface [Windows Shell],Notify method, ICommDlgBrowser2.Notify, ICommDlgBrowser2::Notify, Notify, Notify method [Windows Shell], Notify method [Windows Shell],ICommDlgBrowser2 interface, _win32_ICommDlgBrowser2_Notify, shell.ICommDlgBrowser2_Notify, shobjidl_core/ICommDlgBrowser2::Notify
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
 - ICommDlgBrowser2::Notify
 - shobjidl_core/ICommDlgBrowser2::Notify
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
 - ICommDlgBrowser2.Notify
---

# ICommDlgBrowser2::Notify


## -description

Called by a Shell view to notify the common dialog box hosting it that an event has occurred.

## -parameters

### -param ppshv

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface of the hosted view.

### -param dwNotifyType

Type: <b>DWORD</b>

A flag that can take one of the following two values.



#### CDB2N_CONTEXTMENU_START

Indicates that the shortcut menu is about to be displayed.



#### CDB2N_CONTEXTMENU_DONE

Indicates that the shortcut menu is no longer displayed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>