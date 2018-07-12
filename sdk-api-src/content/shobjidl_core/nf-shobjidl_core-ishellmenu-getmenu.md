---
UID: NF:shobjidl_core.IShellMenu.GetMenu
title: IShellMenu::GetMenu
author: windows-sdk-content
description: Gets the menu information set by calling IShellMenu::SetMenu.
old-location: shell\IShellMenu_GetMenu.htm
old-project: shell
ms.assetid: b366d9c9-5dd3-43ee-99a1-417b9d907855
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetMenu, GetMenu method [Windows Shell], GetMenu method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetMenu method, IShellMenu.GetMenu, IShellMenu::GetMenu, _shell_IShellMenu_GetMenu, shell.IShellMenu_GetMenu, shobjidl_core/IShellMenu::GetMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu.GetMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IShellMenu::GetMenu


## -description


Gets the menu information set by calling <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>.


## -parameters




### -param phmenu [out]

Type: <b>HMENU*</b>

When this method returns, contains a pointer to an <b>HMENU</b> value that receives the <i>hmenu</i> value that you specified when you called <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.


### -param phwnd [out]

Type: <b>HWND*</b>

When this method returns, contains a pointer to an <b>HWND</b> value that receives the <i>hwnd</i> value that you specified when you called <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.


### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to a <b>DWORD</b> value that receives the <i>dwFlags</i> value that you specified when you called <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



