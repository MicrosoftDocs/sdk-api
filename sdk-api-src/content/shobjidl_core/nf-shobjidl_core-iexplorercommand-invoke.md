---
UID: NF:shobjidl_core.IExplorerCommand.Invoke
title: IExplorerCommand::Invoke
author: windows-sdk-content
description: Invokes a Windows Explorer command.
old-location: shell\IExplorerCommand_Invoke.htm
tech.root: shell
ms.assetid: 3ea545a4-5f4c-4f98-9e56-b7c7eed5f821
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IExplorerCommand interface [Windows Shell],Invoke method, IExplorerCommand.Invoke, IExplorerCommand::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],IExplorerCommand interface, _shell_IExplorerCommand_Invoke, shell.IExplorerCommand_Invoke, shobjidl_core/IExplorerCommand::Invoke
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
 - IExplorerCommand.Invoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand::Invoke


## -description


Invokes a Windows Explorer command.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface, which provides access to a bind context. This value can be <b>NULL</b> if no bind context is needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



