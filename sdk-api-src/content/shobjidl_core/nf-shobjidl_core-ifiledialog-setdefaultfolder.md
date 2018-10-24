---
UID: NF:shobjidl_core.IFileDialog.SetDefaultFolder
title: IFileDialog::SetDefaultFolder
author: windows-sdk-content
description: Sets the folder used as a default if there is not a recently used folder value available.
old-location: shell\IFileDialog_SetDefaultFolder.htm
tech.root: shell
ms.assetid: dcde0f80-8118-479d-a08c-4b9af6aa343a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFileDialog interface [Windows Shell],SetDefaultFolder method, IFileDialog.SetDefaultFolder, IFileDialog::SetDefaultFolder, SetDefaultFolder, SetDefaultFolder method [Windows Shell], SetDefaultFolder method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetDefaultFolder, shell_IFileDialog_SetDefaultFolder, shobjidl_core/IFileDialog::SetDefaultFolder
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
 - IFileDialog.SetDefaultFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::SetDefaultFolder


## -description


Sets the folder used as a default if there is not a recently used folder value available.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the interface that represents the folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



