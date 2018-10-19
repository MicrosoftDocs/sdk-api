---
UID: NF:shobjidl_core.IExplorerCommand.GetIcon
title: IExplorerCommand::GetIcon
author: windows-sdk-content
description: Gets an icon resource string of the icon associated with the specified Windows Explorer command item.
old-location: shell\IExplorerCommand_GetIcon.htm
tech.root: shell
ms.assetid: e71b6748-84fc-4944-90b8-a5b0bf97079d
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetIcon, GetIcon method [Windows Shell], GetIcon method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetIcon method, IExplorerCommand.GetIcon, IExplorerCommand::GetIcon, _shell_IExplorerCommand_GetIcon, shell.IExplorerCommand_GetIcon, shobjidl_core/IExplorerCommand::GetIcon
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
 - IExplorerCommand.GetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand::GetIcon


## -description


Gets an icon resource string of the icon associated with the specified Windows Explorer command item.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


### -param ppszIcon [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the resource string that identifies the icon source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The retrieved icon resource string is in the standard format, for instance "shell32.dll,-249".



