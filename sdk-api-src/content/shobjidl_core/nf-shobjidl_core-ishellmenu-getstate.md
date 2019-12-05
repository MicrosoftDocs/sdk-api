---
UID: NF:shobjidl_core.IShellMenu.GetState
title: IShellMenu::GetState (shobjidl_core.h)
description: Gets a filled SMDATA structure.
old-location: shell\IShellMenu_GetState.htm
tech.root: shell
ms.assetid: ea5d402f-2644-4e42-b1e7-2304f0ca71e2
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetState method, IShellMenu.GetState, IShellMenu::GetState, _shell_IShellMenu_GetState, shell.IShellMenu_GetState, shobjidl_core/IShellMenu::GetState
ms.topic: method
f1_keywords:
- shobjidl_core/IShellMenu.GetState
dev_langs:
- c++
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
- IShellMenu.GetState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellMenu::GetState


## -description


Gets a filled <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure.


## -parameters




### -param psmd [out]

Type: <b>LPSMDATA</b>

When this method returns, contains a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure that contains information about the menu band.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



