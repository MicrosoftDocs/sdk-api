---
UID: NF:shobjidl_core.IShellMenu.GetState
title: IShellMenu::GetState
author: windows-sdk-content
description: Gets a filled SMDATA structure.
old-location: shell\IShellMenu_GetState.htm
tech.root: shell
ms.assetid: ea5d402f-2644-4e42-b1e7-2304f0ca71e2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetState, GetState method [Windows Shell], GetState method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetState method, IShellMenu.GetState, IShellMenu::GetState, _shell_IShellMenu_GetState, shell.IShellMenu_GetState, shobjidl_core/IShellMenu::GetState
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
 - IShellMenu.GetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellMenu::GetState


## -description


Gets a filled <a href="https://msdn.microsoft.com/4690daa1-f935-4d0c-8b1f-0b9442fc78dc">SMDATA</a> structure.


## -parameters




### -param psmd [out]

Type: <b>LPSMDATA</b>

When this method returns, contains a pointer to an <a href="https://msdn.microsoft.com/4690daa1-f935-4d0c-8b1f-0b9442fc78dc">SMDATA</a> structure that contains information about the menu band.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



