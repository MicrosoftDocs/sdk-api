---
UID: NF:shobjidl_core.ITaskbarList4.SetTabProperties
title: ITaskbarList4::SetTabProperties (shobjidl_core.h)
description: Allows a tab to specify whether the main application frame window or the tab window should be used as a thumbnail or in the peek feature under certain circumstances.
helpviewer_keywords: ["ITaskbarList4 interface [Windows Shell]","SetTabProperties method","ITaskbarList4.SetTabProperties","ITaskbarList4::SetTabProperties","SetTabProperties","SetTabProperties method [Windows Shell]","SetTabProperties method [Windows Shell]","ITaskbarList4 interface","_shell_ITaskbarList4_SetTabProperties","shell.ITaskbarList4_SetTabProperties","shobjidl_core/ITaskbarList4::SetTabProperties"]
old-location: shell\ITaskbarList4_SetTabProperties.htm
tech.root: shell
ms.assetid: cc3fec4b-7770-44af-9892-239a17dd96b8
ms.date: 12/05/2018
ms.keywords: ITaskbarList4 interface [Windows Shell],SetTabProperties method, ITaskbarList4.SetTabProperties, ITaskbarList4::SetTabProperties, SetTabProperties, SetTabProperties method [Windows Shell], SetTabProperties method [Windows Shell],ITaskbarList4 interface, _shell_ITaskbarList4_SetTabProperties, shell.ITaskbarList4_SetTabProperties, shobjidl_core/ITaskbarList4::SetTabProperties
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList4::SetTabProperties
 - shobjidl_core/ITaskbarList4::SetTabProperties
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
 - ITaskbarList4.SetTabProperties
---

# ITaskbarList4::SetTabProperties


## -description

Allows a tab to specify whether the main application frame window or the tab window should be used as a thumbnail or in the peek feature under certain circumstances.

## -parameters

### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window that is to have properties set. This handle must already be registered through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">RegisterTab</a>.

### -param stpFlags [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag">STPFLAG</a></b>

One or more members of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag">STPFLAG</a> enumeration that specify the displayed thumbnail and peek image source of the tab thumbnail.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An application might want to use the thumbnail or peek representation of its associated parent window if the application cannot generate its own thumbnail for a tab or for its active tab content (such as an animation) to appear live.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4">ITaskbarList4</a>