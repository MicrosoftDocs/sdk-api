---
UID: NF:shobjidl_core.IShellMenu.InvalidateItem
title: IShellMenu::InvalidateItem
author: windows-sdk-content
description: Redraws an item in a menu band.
old-location: shell\IShellMenu_InvalidateItem.htm
tech.root: shell
ms.assetid: 694722f2-2030-4c85-bcc4-70f8a8b70161
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IShellMenu interface [Windows Shell],InvalidateItem method, IShellMenu.InvalidateItem, IShellMenu::InvalidateItem, InvalidateItem, InvalidateItem method [Windows Shell], InvalidateItem method [Windows Shell],IShellMenu interface, _shell_IShellMenu_InvalidateItem, shell.IShellMenu_InvalidateItem, shobjidl_core/IShellMenu::InvalidateItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu.InvalidateItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellMenu::InvalidateItem


## -description


Redraws an item in a menu band.


## -parameters




### -param psmd [in]

Type: <b>LPSMDATA</b>

A pointer to an <a href="https://msdn.microsoft.com/4690daa1-f935-4d0c-8b1f-0b9442fc78dc">SMDATA</a> structure that identifies the item to be redrawn. Set this value to <b>NULL</b> to redraw the entire menu.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that control how the menu is redrawn. If <i>psmd</i> is <b>NULL</b>, set <i>dwFlags</i> to SMINV_REFRESH. If <i>psmd</i> is set to a valid <a href="https://msdn.microsoft.com/4690daa1-f935-4d0c-8b1f-0b9442fc78dc">SMDATA</a> structure, set <i>dwFlags</i> to SMINV_ID | SMINV_REFRESH.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



