---
UID: NF:shobjidl_core.IExecuteCommand.SetNoShowUI
title: IExecuteCommand::SetNoShowUI
author: windows-sdk-content
description: Indicates whether any UI associated with the selected Shell item should be displayed.
old-location: shell\IExecuteCommand_SetNoShowUI.htm
tech.root: shell
ms.assetid: 26cec8f2-984a-4358-9082-bf6b886690eb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetNoShowUI method, IExecuteCommand.SetNoShowUI, IExecuteCommand::SetNoShowUI, SetNoShowUI, SetNoShowUI method [Windows Shell], SetNoShowUI method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetNoShowUI, shell.IExecuteCommand_SetNoShowUI, shobjidl_core/IExecuteCommand::SetNoShowUI
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
 - IExecuteCommand.SetNoShowUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExecuteCommand::SetNoShowUI


## -description


Indicates whether any UI associated with the selected Shell item should be displayed.


## -parameters




### -param fNoShowUI [in]

Type: <b>BOOL</b>

<b>TRUE</b> to block display of any associated UI; <b>FALSE</b> to display the UI. <b>FALSE</b> is the default value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



