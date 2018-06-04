---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



