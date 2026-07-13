---
UID: NF:shobjidl_core.ITaskbarList3.SetTabOrder
title: ITaskbarList3::SetTabOrder (shobjidl_core.h)
description: Inserts a new thumbnail into a tabbed-document interface (TDI) or multiple-document interface (MDI) application's group flyout or moves an existing thumbnail to a new position in the application's group.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","SetTabOrder method","ITaskbarList3.SetTabOrder","ITaskbarList3::SetTabOrder","SetTabOrder","SetTabOrder method [Windows Shell]","SetTabOrder method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_SetTabOrder","shell.ITaskbarList3_SetTabOrder","shobjidl_core/ITaskbarList3::SetTabOrder"]
old-location: shell\ITaskbarList3_SetTabOrder.htm
tech.root: shell
ms.assetid: a35342fd-448b-48cf-8400-30f4b7776bbf
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetTabOrder method, ITaskbarList3.SetTabOrder, ITaskbarList3::SetTabOrder, SetTabOrder, SetTabOrder method [Windows Shell], SetTabOrder method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetTabOrder, shell.ITaskbarList3_SetTabOrder, shobjidl_core/ITaskbarList3::SetTabOrder
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
 - ITaskbarList3::SetTabOrder
 - shobjidl_core/ITaskbarList3::SetTabOrder
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
 - ITaskbarList3.SetTabOrder
---

# ITaskbarList3::SetTabOrder


## -description

Inserts a new thumbnail into a tabbed-document interface (TDI) or multiple-document interface (MDI) application's group flyout or moves an existing thumbnail to a new position in the application's group.

## -parameters

### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window whose thumbnail is being placed. This value is required, must already be registered through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>, and cannot be <b>NULL</b>.

### -param hwndInsertBefore [in, optional]

Type: <b>HWND</b>

The handle of the tab window whose thumbnail that <i>hwndTab</i> is inserted to the left of. This handle must already be registered through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>. If this value is <b>NULL</b>, the new thumbnail is added to the end of the list.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method must be called for the thumbnail to be shown in the group. Call it after you have called <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive">ITaskbarList3::SetTabActive</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab">ITaskbarList3::UnregisterTab</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>