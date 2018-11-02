---
UID: NF:shobjidl_core.IShellLinkW.GetShowCmd
title: IShellLinkW::GetShowCmd
author: windows-sdk-content
description: Gets the show command for a Shell link object.
old-location: shell\IShellLink_GetShowCmd.htm
tech.root: shell
ms.assetid: cbd89c28-86e1-4a2c-b3ea-d934f263b59f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetShowCmd, GetShowCmd method [Windows Shell], GetShowCmd method [Windows Shell],IShellLink interface, GetShowCmd method [Windows Shell],IShellLinkA interface, GetShowCmd method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetShowCmd method, IShellLink::GetShowCmd, IShellLinkA interface [Windows Shell],GetShowCmd method, IShellLinkA::GetShowCmd, IShellLinkW interface [Windows Shell],GetShowCmd method, IShellLinkW.GetShowCmd, IShellLinkW::GetShowCmd, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWNORMAL, _win32_IShellLink_GetShowCmd, shell.IShellLink_GetShowCmd, shobjidl_core/IShellLink::GetShowCmd, shobjidl_core/IShellLinkA::GetShowCmd, shobjidl_core/IShellLinkW::GetShowCmd
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
 - IShellLink.GetShowCmd
 - IShellLinkA.GetShowCmd
 - IShellLinkW.GetShowCmd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkW::GetShowCmd


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


##### - piShowCmd.SW_SHOWMAXIMIZED

Activates the window and displays it as a maximized window.


##### - piShowCmd.SW_SHOWMINIMIZED

Activates the window and displays it as a minimized window.


##### - piShowCmd.SW_SHOWNORMAL

Activates and displays a window. If the window is minimized or maximized, the system restores it to its original size and position. An application should specify this flag when displaying the window for the first time.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The show command is used to set the initial show state of the corresponding object. This is one of the SW_xxx values described in <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>.




## -see-also




<a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a>



<a href="https://msdn.microsoft.com/9f40cd7d-04b5-4880-831f-5fb5cd52a2eb">IShellLink::SetShowCmd</a>



<b>IShellLinkA</b>



<b>IShellLinkW</b>
 

 

