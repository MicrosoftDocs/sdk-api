---
UID: NF:shobjidl_core.IExplorerCommand.GetToolTip
title: IExplorerCommand::GetToolTip (shobjidl_core.h)
author: windows-sdk-content
description: Gets the tooltip string associated with a specified Windows Explorer command item.
old-location: shell\IExplorerCommand_GetToolTip.htm
tech.root: shell
ms.assetid: f2c54602-2ffc-45bc-ba00-d7b9d4cf2343
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetToolTip, GetToolTip method [Windows Shell], GetToolTip method [Windows Shell],IExplorerCommand interface, IExplorerCommand interface [Windows Shell],GetToolTip method, IExplorerCommand.GetToolTip, IExplorerCommand::GetToolTip, _shell_IExplorerCommand_GetToolTip, shell.IExplorerCommand_GetToolTip, shobjidl_core/IExplorerCommand::GetToolTip
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
 - IExplorerCommand.GetToolTip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerCommand::GetToolTip


## -description


Gets the tooltip string associated with a specified Windows Explorer command item.


## -parameters




### -param psiItemArray [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.


### -param ppszInfotip [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the tooltip string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



