---
UID: NF:shobjidl_core.IExecuteCommand.SetKeyState
title: IExecuteCommand::SetKeyState
author: windows-sdk-content
description: Sets a value based on the current state of the keys CTRL and SHIFT.
old-location: shell\IExecuteCommand_SetKeyState.htm
tech.root: shell
ms.assetid: 66f051a1-eb45-43c1-bf09-4be6ca2a1c7c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetKeyState method, IExecuteCommand.SetKeyState, IExecuteCommand::SetKeyState, MK_CONTROL, MK_SHIFT, SetKeyState, SetKeyState method [Windows Shell], SetKeyState method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetKeyState, shell.IExecuteCommand_SetKeyState, shobjidl_core/IExecuteCommand::SetKeyState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IExecuteCommand.SetKeyState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExecuteCommand::SetKeyState


## -description


Sets a value based on the current state of the keys CTRL and SHIFT.


## -parameters




### -param grfKeyState [in]

Type: <b>DWORD</b>

One or both of the following flags to indicate whether the key is pressed.



#### MK_CONTROL

The CTRL key is pressed.



#### MK_SHIFT

The SHIFT key is pressed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



