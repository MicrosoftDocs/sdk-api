---
UID: NF:shobjidl_core.INameSpaceTreeControl.SetTheme
title: INameSpaceTreeControl::SetTheme
author: windows-sdk-content
description: Sets the desktop theme for the current window only.
old-location: shell\INameSpaceTreeControl_SetTheme.htm
tech.root: shell
ms.assetid: 1b518d58-716b-4ae1-8633-e43117363541
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],SetTheme method, INameSpaceTreeControl.SetTheme, INameSpaceTreeControl::SetTheme, SetTheme, SetTheme method [Windows Shell], SetTheme method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_SetTheme, shell.INameSpaceTreeControl_SetTheme, shobjidl_core/INameSpaceTreeControl::SetTheme
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.SetTheme
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



