---
UID: NF:shobjidl_core.ITaskbarList3.UnregisterTab
title: ITaskbarList3::UnregisterTab (shobjidl_core.h)
description: Removes a thumbnail from an application's preview group when that tab or document is closed in the application.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","UnregisterTab method","ITaskbarList3.UnregisterTab","ITaskbarList3::UnregisterTab","UnregisterTab","UnregisterTab method [Windows Shell]","UnregisterTab method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_UnregisterTab","shell.ITaskbarList3_UnregisterTab","shobjidl_core/ITaskbarList3::UnregisterTab"]
old-location: shell\ITaskbarList3_UnregisterTab.htm
tech.root: shell
ms.assetid: 667cafde-f693-46c3-bbec-140fc7cade5d
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],UnregisterTab method, ITaskbarList3.UnregisterTab, ITaskbarList3::UnregisterTab, UnregisterTab, UnregisterTab method [Windows Shell], UnregisterTab method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_UnregisterTab, shell.ITaskbarList3_UnregisterTab, shobjidl_core/ITaskbarList3::UnregisterTab
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList3::UnregisterTab
 - shobjidl_core/ITaskbarList3::UnregisterTab
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.UnregisterTab
---

# ITaskbarList3::UnregisterTab


## -description

Removes a thumbnail from an application's preview group when that tab or document is closed in the application.

## -parameters

### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window whose thumbnail is being removed. This is the same value with which the thumbnail was registered as part the group through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>. This value is required and cannot be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise. If <i>hwndTab</i> is <b>NULL</b>, this method returns an error.

## -remarks

It is the responsibility of the calling application to free <i>hwndTab</i> through <a href="/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a>. <b>UnregisterTab</b> must be called before the handle is freed.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive">ITaskbarList3::SetTabActive</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder">ITaskbarList3::SetTabOrder</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>