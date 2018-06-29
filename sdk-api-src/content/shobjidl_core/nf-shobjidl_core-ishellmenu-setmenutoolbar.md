---
UID: NF:shobjidl_core.IShellMenu.SetMenuToolbar
title: IShellMenu::SetMenuToolbar
author: windows-sdk-content
description: Adds a menu to the menuband.
old-location: shell\IShellMenu_SetMenuToolbar.htm
old-project: shell
ms.assetid: 6067f2be-883a-4271-95ad-16fd868b37a0
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IShellMenu interface [Windows Shell],SetMenuToolbar method, IShellMenu.SetMenuToolbar, IShellMenu::SetMenuToolbar, SMSET_BOTTOM, SMSET_DONTOWN, SMSET_TOP, SetMenuToolbar, SetMenuToolbar method [Windows Shell], SetMenuToolbar method [Windows Shell],IShellMenu interface, _shell_IShellMenu_SetMenuToolbar, shell.IShellMenu_SetMenuToolbar, shobjidl_core/IShellMenu::SetMenuToolbar
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
 - IShellMenu.SetMenuToolbar
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IShellMenu::SetMenuToolbar


## -description


Adds a menu to the menuband.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an object that supports <b>CLSID_MenuToolbarBase</b> in its <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that control how the menu operates.



#### SMSET_TOP

Bias this namespace to the top of the menu.




#### SMSET_BOTTOM

Bias this namespace to the bottom of the menu.



#### SMSET_DONTOWN

The Menuband does not own the non-ref counted object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



