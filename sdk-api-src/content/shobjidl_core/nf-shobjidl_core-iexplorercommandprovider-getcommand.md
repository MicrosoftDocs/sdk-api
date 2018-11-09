---
UID: NF:shobjidl_core.IExplorerCommandProvider.GetCommand
title: IExplorerCommandProvider::GetCommand
author: windows-sdk-content
description: Gets a specified Explorer command instance.
old-location: shell\IExplorerCommandProvider_GetCommand.htm
tech.root: shell
ms.assetid: 8ef1fb9d-03ed-4e1a-bc13-9f5caab2abb9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCommand, GetCommand method [Windows Shell], GetCommand method [Windows Shell],IExplorerCommandProvider interface, IExplorerCommandProvider interface [Windows Shell],GetCommand method, IExplorerCommandProvider.GetCommand, IExplorerCommandProvider::GetCommand, _shell_IExplorerCommandProvider_GetCommand, shell.IExplorerCommandProvider_GetCommand, shobjidl_core/IExplorerCommandProvider::GetCommand
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
 - IExplorerCommandProvider.GetCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommandProvider::GetCommand


## -description


Gets a specified Explorer command instance.


## -parameters




### -param rguidCommandId

Type: <b>REFGUID</b>

A reference to a command ID as a <b>GUID</b>. Used to obtain a command definition.


### -param riid

Type: <b>REFIID</b>

A reference to the IID of the requested interface.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in riid. This will typically be <a href="https://msdn.microsoft.com/61e94e50-9e12-4a2c-a6c7-64a9181f80b8">IExplorerCommand</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



