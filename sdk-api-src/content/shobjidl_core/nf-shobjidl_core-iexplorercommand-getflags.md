---
UID: NF:shobjidl_core.IExplorerCommand.GetFlags
title: IExplorerCommand::GetFlags (shobjidl_core.h)
description: Gets the flags associated with a Windows Explorer command.
helpviewer_keywords: ["ECF_AUTOMENUICONS","ECF_DEFAULT","ECF_HASLUASHIELD","ECF_HASSPLITBUTTON","ECF_HASSUBCOMMANDS","ECF_HIDELABEL","ECF_ISDROPDOWN","ECF_ISSEPARATOR","ECF_SEPARATORAFTER","ECF_SEPARATORBEFORE","ECF_TOGGLEABLE","GetFlags","GetFlags method [Windows Shell]","GetFlags method [Windows Shell]","IExplorerCommand interface","IExplorerCommand interface [Windows Shell]","GetFlags method","IExplorerCommand.GetFlags","IExplorerCommand::GetFlags","_shell_IExplorerCommand_GetFlags","shell.IExplorerCommand_GetFlags","shobjidl_core/IExplorerCommand::GetFlags"]
old-location: shell\IExplorerCommand_GetFlags.htm
tech.root: shell
ms.assetid: cd0a01fa-2525-4296-b77d-bba3fb80472d
ms.date: 12/05/2018
ms.keywords: ECF_AUTOMENUICONS, ECF_DEFAULT, ECF_HASLUASHIELD, ECF_HASSPLITBUTTON, ECF_HASSUBCOMMANDS, ECF_HIDELABEL, ECF_ISDROPDOWN, ECF_ISSEPARATOR, ECF_SEPARATORAFTER, ECF_SEPARATORBEFORE, ECF_TOGGLEABLE, GetFlags, GetFlags method [Windows Shell], GetFlags method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetFlags method, IExplorerCommand.GetFlags, IExplorerCommand::GetFlags, _shell_IExplorerCommand_GetFlags, shell.IExplorerCommand_GetFlags, shobjidl_core/IExplorerCommand::GetFlags
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
 - IExplorerCommand::GetFlags
 - shobjidl_core/IExplorerCommand::GetFlags
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
 - IExplorerCommand.GetFlags
---

# IExplorerCommand::GetFlags


## -description

Gets the flags associated with a Windows Explorer command.

## -parameters

### -param pFlags [out]

Type: <b>EXPCMDFLAGS*</b>

When this method returns, this value points to the current command flags. One of more of the following values:



#### ECF_DEFAULT (0x000)

<b>Windows 7 and later</b>. No command flags are set.



#### ECF_HASSUBCOMMANDS (0x001)

The command has subcommands.



#### ECF_HASSPLITBUTTON (0x002)

A split button is displayed.



#### ECF_HIDELABEL (0x004)

The label is hidden.



#### ECF_ISSEPARATOR (0x008)

The command is a separator.



#### ECF_HASLUASHIELD (0x010)

A UAC shield is displayed.



#### ECF_SEPARATORBEFORE (0x020)

<b>Introduced in Windows 7</b>. The command is located in the menu immediately below a separator.



#### ECF_SEPARATORAFTER (0x040)

<b>Introduced in Windows 7</b>. The command is located in the menu immediately above a separator.



#### ECF_ISDROPDOWN (0x080)

<b>Introduced in Windows 7</b>. Selecting the command opens a drop-down submenu (for example, <b>Include in library</b>).



#### ECF_TOGGLEABLE (0x100)

<b>Introduced in Windows 8</b>.



#### ECF_AUTOMENUICONS (0x200)

<b>Introduced in Windows 8</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

