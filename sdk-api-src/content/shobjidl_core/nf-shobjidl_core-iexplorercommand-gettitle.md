---
UID: NF:shobjidl_core.IExplorerCommand.GetTitle
title: IExplorerCommand::GetTitle
author: windows-sdk-content
description: Gets the title text of the button or menu item that launches a specified Windows Explorer command item.
old-location: shell\IExplorerCommand_GetTitle.htm
tech.root: shell
ms.assetid: d03ca4c5-80a5-4b7d-a47b-a67c72b7883c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTitle, GetTitle method [Windows Shell], GetTitle method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetTitle method, IExplorerCommand.GetTitle, IExplorerCommand::GetTitle, _shell_IExplorerCommand_GetTitle, shell.IExplorerCommand_GetTitle, shobjidl_core/IExplorerCommand::GetTitle
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
 - IExplorerCommand.GetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand::GetTitle


## -description


Gets the title text of the button or menu item that launches a specified Windows Explorer command item.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


### -param ppszName [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the title string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



