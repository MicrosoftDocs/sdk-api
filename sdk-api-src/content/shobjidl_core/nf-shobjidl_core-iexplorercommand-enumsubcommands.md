---
UID: NF:shobjidl_core.IExplorerCommand.EnumSubCommands
title: IExplorerCommand::EnumSubCommands (shobjidl_core.h)
description: Retrieves an enumerator for a command's subcommands.
helpviewer_keywords: ["EnumSubCommands","EnumSubCommands method [Windows Shell]","EnumSubCommands method [Windows Shell]","IExplorerCommand interface","IExplorerCommand interface [Windows Shell]","EnumSubCommands method","IExplorerCommand.EnumSubCommands","IExplorerCommand::EnumSubCommands","_shell_IExplorerCommand_EnumSubCommands","shell.IExplorerCommand_EnumSubCommands","shobjidl_core/IExplorerCommand::EnumSubCommands"]
old-location: shell\IExplorerCommand_EnumSubCommands.htm
tech.root: shell
ms.assetid: c907fb46-fb18-431c-861b-c2d2270a89b9
ms.date: 12/05/2018
ms.keywords: EnumSubCommands, EnumSubCommands method [Windows Shell], EnumSubCommands method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],EnumSubCommands method, IExplorerCommand.EnumSubCommands, IExplorerCommand::EnumSubCommands, _shell_IExplorerCommand_EnumSubCommands, shell.IExplorerCommand_EnumSubCommands, shobjidl_core/IExplorerCommand::EnumSubCommands
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
 - IExplorerCommand::EnumSubCommands
 - shobjidl_core/IExplorerCommand::EnumSubCommands
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
 - IExplorerCommand.EnumSubCommands
---

# IExplorerCommand::EnumSubCommands


## -description

Retrieves an enumerator for a command's subcommands.

## -parameters

### -param ppEnum [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand">IEnumExplorerCommand</a>**</b>

When this method returns successfully, contains an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand">IEnumExplorerCommand</a> interface pointer that can be used to walk the set of subcommands.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Subcommands are displayed as menu drop-down items through the use of a Split button when commands are exposed at the top of a Windows Explorer window. In that position, only the default command button is given an icon. In a normal menu, the icons for all commands are shown.

Subcommands which themselves have subcommands are not supported by Windows Explorer. When a command has its own subcommands, it must designate this status by specifying ECF_HASSUBCOMMANDS in the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags">IExplorerCommand::GetFlags</a> call.