---
UID: NF:shobjidl_core.IShellLinkA.GetShowCmd
title: IShellLinkA::GetShowCmd (shobjidl_core.h)
description: Gets the show command for a Shell link object. (ANSI)
helpviewer_keywords: ["GetShowCmd","GetShowCmd method [Windows Shell]","GetShowCmd method [Windows Shell]","IShellLink interface","GetShowCmd method [Windows Shell]","IShellLinkA interface","GetShowCmd method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetShowCmd method","IShellLink::GetShowCmd","IShellLinkA interface [Windows Shell]","GetShowCmd method","IShellLinkA.GetShowCmd","IShellLinkA::GetShowCmd","IShellLinkW interface [Windows Shell]","GetShowCmd method","IShellLinkW::GetShowCmd","SW_SHOWMAXIMIZED","SW_SHOWMINIMIZED","SW_SHOWNORMAL","_win32_IShellLink_GetShowCmd","shell.IShellLink_GetShowCmd","shobjidl_core/IShellLink::GetShowCmd","shobjidl_core/IShellLinkA::GetShowCmd","shobjidl_core/IShellLinkW::GetShowCmd"]
old-location: shell\IShellLink_GetShowCmd.htm
tech.root: shell
ms.assetid: cbd89c28-86e1-4a2c-b3ea-d934f263b59f
ms.date: 12/05/2018
ms.keywords: GetShowCmd, GetShowCmd method [Windows Shell], GetShowCmd method [Windows Shell],IShellLink interface, GetShowCmd method [Windows Shell],IShellLinkA interface, GetShowCmd method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetShowCmd method, IShellLink::GetShowCmd, IShellLinkA interface [Windows Shell],GetShowCmd method, IShellLinkA.GetShowCmd, IShellLinkA::GetShowCmd, IShellLinkW interface [Windows Shell],GetShowCmd method, IShellLinkW::GetShowCmd, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWNORMAL, _win32_IShellLink_GetShowCmd, shell.IShellLink_GetShowCmd, shobjidl_core/IShellLink::GetShowCmd, shobjidl_core/IShellLinkA::GetShowCmd, shobjidl_core/IShellLinkW::GetShowCmd
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkA::GetShowCmd
 - shobjidl_core/IShellLinkA::GetShowCmd
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
 - IShellLink.GetShowCmd
 - IShellLinkA.GetShowCmd
 - IShellLinkW.GetShowCmd
---

# IShellLinkA::GetShowCmd


## -description

Gets the show command for a Shell link object.

## -parameters

### -param piShowCmd

Type: <b>int*</b>

A pointer to the command. The following commands are supported.



#### SW_SHOWNORMAL

Activates and displays a window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when displaying the window for the first time.



#### SW_SHOWMAXIMIZED

Activates the window and displays it as a maximized window.



#### SW_SHOWMINIMIZED

Activates the window and displays it as a minimized window.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The show command is used to set the initial show state of the corresponding object. This is one of the SW_xxx values described in <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd">IShellLink::SetShowCmd</a>



<b>IShellLinkA</b>



<b>IShellLinkW</b>
