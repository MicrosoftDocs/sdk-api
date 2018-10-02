---
UID: NF:shobjidl_core.IShellLinkA.SetShowCmd
title: IShellLinkA::SetShowCmd
author: windows-sdk-content
description: Sets the show command for a Shell link object. The show command sets the initial show state of the window.
old-location: shell\IShellLink_SetShowCmd.htm
tech.root: Shell
ms.assetid: 9f40cd7d-04b5-4880-831f-5fb5cd52a2eb
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IShellLink interface [Windows Shell],SetShowCmd method, IShellLink::SetShowCmd, IShellLinkA interface [Windows Shell],SetShowCmd method, IShellLinkA.SetShowCmd, IShellLinkA::SetShowCmd, IShellLinkW interface [Windows Shell],SetShowCmd method, IShellLinkW::SetShowCmd, SW_SHOWMAXIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNORMAL, SetShowCmd, SetShowCmd method [Windows Shell], SetShowCmd method [Windows Shell],IShellLink interface, SetShowCmd method [Windows Shell],IShellLinkA interface, SetShowCmd method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetShowCmd, shell.IShellLink_SetShowCmd, shobjidl_core/IShellLink::SetShowCmd, shobjidl_core/IShellLinkA::SetShowCmd, shobjidl_core/IShellLinkW::SetShowCmd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLink.SetShowCmd
 - IShellLinkA.SetShowCmd
 - IShellLinkW.SetShowCmd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkA::SetShowCmd


## -description


Sets the show command for a Shell link object. The show command sets the initial show state of the window.


## -parameters




### -param iShowCmd

Type: <b>int</b>

Command. <b>SetShowCmd</b> accepts one of the following <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a> commands.



#### SW_SHOWNORMAL

Activates and displays a window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when displaying the window for the first time.



#### SW_SHOWMAXIMIZED

Activates the window and displays it as a maximized window.



#### SW_SHOWMINNOACTIVE

Displays the window in its minimized state, leaving the currently active window as active.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a>



<a href="https://msdn.microsoft.com/cbd89c28-86e1-4a2c-b3ea-d934f263b59f">IShellLink::GetShowCmd</a>



<b>IShellLinkA</b>



<b>IShellLinkW</b>
 

 

