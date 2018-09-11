---
UID: NF:shobjidl_core.IExplorerCommand.GetCanonicalName
title: IExplorerCommand::GetCanonicalName
author: windows-sdk-content
description: Gets the GUID of an Windows Explorer command.
old-location: shell\IExplorerCommand_GetCanonicalName.htm
tech.root: shell
ms.assetid: c0f2fc66-98f5-404f-9d82-0290ed235ac0
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetCanonicalName, GetCanonicalName method [Windows Shell], GetCanonicalName method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetCanonicalName method, IExplorerCommand.GetCanonicalName, IExplorerCommand::GetCanonicalName, _shell_IExplorerCommand_GetCanonicalName, shell.IExplorerCommand_GetCanonicalName, shobjidl_core/IExplorerCommand::GetCanonicalName
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
 - IExplorerCommand.GetCanonicalName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand::GetCanonicalName


## -description


Gets the GUID of an Windows Explorer command.


## -parameters




### -param pguidCommandName [out]

Type: <b>GUID*</b>

A pointer to a value that, when this method returns successfully, receives the command's GUID, under which it is declared in the registry.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is somewhat misnamed, given that it retrieves a GUID. To retrieve the command's canonical name, you must take the additional step to pull it from the command's subkey. The GUID is the name of the subkey. where that information is stored.



