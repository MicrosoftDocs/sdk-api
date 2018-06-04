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



