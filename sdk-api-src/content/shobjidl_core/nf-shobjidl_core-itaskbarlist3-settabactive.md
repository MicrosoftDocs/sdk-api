---
UID: NF:shobjidl_core.ITaskbarList3.SetTabActive
title: ITaskbarList3::SetTabActive (shobjidl_core.h)
author: windows-sdk-content
description: Informs the taskbar that a tab or document window has been made the active window.
old-location: shell\ITaskbarList3_SetTabActive.htm
tech.root: shell
ms.assetid: d82f11eb-bfff-4661-8e2e-520f8226809b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],SetTabActive method, ITaskbarList3.SetTabActive, ITaskbarList3::SetTabActive, SetTabActive, SetTabActive method [Windows Shell], SetTabActive method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_SetTabActive, shell.ITaskbarList3_SetTabActive, shobjidl_core/ITaskbarList3::SetTabActive
ms.topic: method
f1_keywords: 
 - "shobjidl_core/ITaskbarList3.SetTabActive"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.SetTabActive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskbarList3::SetTabActive


## -description


Informs the taskbar that a tab or document window has been made the active window.


## -parameters




### -param hwndTab [in]

Type: <b>HWND</b>

Handle of the active tab window. This handle must already be registered through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>. This value can be <b>NULL</b> if no tab is active.


### -param hwndMDI [in]

Type: <b>HWND</b>

Handle of the application's main window. This value tells the taskbar which group the thumbnail is a member of. This value is required and cannot be <b>NULL</b>.


### -param dwReserved [in]

Type: <b>DWORD</b>

Reserved; set to 0.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">ITaskbarList3::RegisterTab</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder">ITaskbarList3::SetTabOrder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab">ITaskbarList3::UnregisterTab</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
 

 

