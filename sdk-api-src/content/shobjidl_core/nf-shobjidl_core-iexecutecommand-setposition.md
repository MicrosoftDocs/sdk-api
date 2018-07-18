---
UID: NF:shobjidl_core.IExecuteCommand.SetPosition
title: IExecuteCommand::SetPosition
author: windows-sdk-content
description: Sets the coordinates of a point used for display.
old-location: shell\IExecuteCommand_SetPosition.htm
old-project: shell
ms.assetid: ead12c05-ce94-494d-9f31-9b0f341363b5
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetPosition method, IExecuteCommand.SetPosition, IExecuteCommand::SetPosition, SetPosition, SetPosition method [Windows Shell], SetPosition method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetPosition, shell.IExecuteCommand_SetPosition, shobjidl_core/IExecuteCommand::SetPosition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExecuteCommand.SetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExecuteCommand::SetPosition


## -description


Sets the coordinates of a point used for display.


## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The screen coordinates at which the user right-clicked to invoke the shortcut menu from which a command was chosen. Applications can use this information to present any UI. This is particularly useful in a multi-monitor situation. The default position is the center of the default monitor.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



