---
UID: NF:shobjidl_core.ITaskbarList3.RegisterTab
title: ITaskbarList3::RegisterTab (shobjidl_core.h)
description: Informs the taskbar that a new tab or document thumbnail has been provided for display in an application's taskbar group flyout.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","RegisterTab method","ITaskbarList3.RegisterTab","ITaskbarList3::RegisterTab","RegisterTab","RegisterTab method [Windows Shell]","RegisterTab method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_RegisterTab","shell.ITaskbarList3_RegisterTab","shobjidl_core/ITaskbarList3::RegisterTab"]
old-location: shell\ITaskbarList3_RegisterTab.htm
tech.root: shell
ms.assetid: b0cdca51-108a-4507-bd9e-6bcd4386c36a
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],RegisterTab method, ITaskbarList3.RegisterTab, ITaskbarList3::RegisterTab, RegisterTab, RegisterTab method [Windows Shell], RegisterTab method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_RegisterTab, shell.ITaskbarList3_RegisterTab, shobjidl_core/ITaskbarList3::RegisterTab
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
 - ITaskbarList3::RegisterTab
 - shobjidl_core/ITaskbarList3::RegisterTab
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
 - ITaskbarList3.RegisterTab
---

# ITaskbarList3::RegisterTab


## -description

Informs the taskbar that a new tab or document thumbnail has been provided for display in an application's taskbar group flyout.

## -parameters

### -param hwndTab [in]

Type: <b>HWND</b>

Handle of the tab or document window. This value is required and cannot be <b>NULL</b>.

### -param hwndMDI [in]

Type: <b>HWND</b>

Handle of the application's main window. This value tells the taskbar which application's preview group to attach the new thumbnail to. This value is required and cannot be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If either parameter is <b>NULL</b>, this method returns an error.

## -remarks

By itself, registering a tab thumbnail alone will not result in its being displayed. You must also call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder">ITaskbarList3::SetTabOrder</a> to instruct the group where to display it.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive">ITaskbarList3::SetTabActive</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder">ITaskbarList3::SetTabOrder</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab">ITaskbarList3::UnregisterTab</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>