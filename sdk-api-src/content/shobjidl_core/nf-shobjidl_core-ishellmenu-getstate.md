---
UID: NF:shobjidl_core.IShellMenu.GetState
title: IShellMenu::GetState (shobjidl_core.h)
description: Gets a filled SMDATA structure.
helpviewer_keywords: ["GetState","GetState method [Windows Shell]","GetState method [Windows Shell]","IShellMenu interface","IShellMenu interface [Windows Shell]","GetState method","IShellMenu.GetState","IShellMenu::GetState","_shell_IShellMenu_GetState","shell.IShellMenu_GetState","shobjidl_core/IShellMenu::GetState"]
old-location: shell\IShellMenu_GetState.htm
tech.root: shell
ms.assetid: ea5d402f-2644-4e42-b1e7-2304f0ca71e2
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetState method, IShellMenu.GetState, IShellMenu::GetState, _shell_IShellMenu_GetState, shell.IShellMenu_GetState, shobjidl_core/IShellMenu::GetState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellMenu::GetState
 - shobjidl_core/IShellMenu::GetState
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
 - IShellMenu.GetState
---

# IShellMenu::GetState


## -description

Gets a filled <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure.

## -parameters

### -param psmd [out]

Type: <b>LPSMDATA</b>

When this method returns, contains a pointer to an <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure that contains information about the menu band.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.