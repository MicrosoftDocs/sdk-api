---
UID: NF:shobjidl_core.IExplorerCommand.EnumSubCommands
title: IExplorerCommand::EnumSubCommands
author: windows-sdk-content
description: Retrieves an enemerator for a command's subcommands.
old-location: shell\IExplorerCommand_EnumSubCommands.htm
tech.root: shell
ms.assetid: c907fb46-fb18-431c-861b-c2d2270a89b9
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: EnumSubCommands, EnumSubCommands method [Windows Shell], EnumSubCommands method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],EnumSubCommands method, IExplorerCommand.EnumSubCommands, IExplorerCommand::EnumSubCommands, _shell_IExplorerCommand_EnumSubCommands, shell.IExplorerCommand_EnumSubCommands, shobjidl_core/IExplorerCommand::EnumSubCommands
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
 - IExplorerCommand.EnumSubCommands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand::EnumSubCommands


## -description


Retrieves an enemerator for a command's subcommands.


## -parameters




### -param ppEnum [out]

Type: <b><a href="https://msdn.microsoft.com/c9a21e84-dd95-413a-b9db-e02008185bef">IEnumExplorerCommand</a>**</b>

When this method returns successfully, contains an <a href="https://msdn.microsoft.com/c9a21e84-dd95-413a-b9db-e02008185bef">IEnumExplorerCommand</a> interface pointer that can be used to walk the set of subcommands.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Subcommands are displayed as menu drop-down items through the use of a Split button when commands are exposed at the top of a Windows Explorer window. In that position, only the default command button is given an icon. In a normal menu, the icons for all commands are shown.

Subcommands which themselves have subcommands are not supported by Windows Explorer. When a command has its own subcommands, it must designate this status by specifying ECF_HASSUBCOMMANDS in the <a href="https://msdn.microsoft.com/cd0a01fa-2525-4296-b77d-bba3fb80472d">IExplorerCommand::GetFlags</a> call.



