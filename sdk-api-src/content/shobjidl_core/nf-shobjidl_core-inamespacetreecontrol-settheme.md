---
UID: NF:shobjidl_core.INameSpaceTreeControl.SetTheme
title: INameSpaceTreeControl::SetTheme (shobjidl_core.h)
description: Sets the desktop theme for the current window only.
helpviewer_keywords: ["INameSpaceTreeControl interface [Windows Shell]","SetTheme method","INameSpaceTreeControl.SetTheme","INameSpaceTreeControl::SetTheme","SetTheme","SetTheme method [Windows Shell]","SetTheme method [Windows Shell]","INameSpaceTreeControl interface","_shell_INameSpaceTreeControl_SetTheme","shell.INameSpaceTreeControl_SetTheme","shobjidl_core/INameSpaceTreeControl::SetTheme"]
old-location: shell\INameSpaceTreeControl_SetTheme.htm
tech.root: shell
ms.assetid: 1b518d58-716b-4ae1-8633-e43117363541
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],SetTheme method, INameSpaceTreeControl.SetTheme, INameSpaceTreeControl::SetTheme, SetTheme, SetTheme method [Windows Shell], SetTheme method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_SetTheme, shell.INameSpaceTreeControl_SetTheme, shobjidl_core/INameSpaceTreeControl::SetTheme
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - INameSpaceTreeControl::SetTheme
 - shobjidl_core/INameSpaceTreeControl::SetTheme
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
 - INameSpaceTreeControl.SetTheme
---

# INameSpaceTreeControl::SetTheme


## -description

Sets the desktop theme for the current window only.

## -parameters

### -param pszTheme [in]

Type: <b>LPCWSTR</b>

The name of the desktop theme to which the current window is being set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

