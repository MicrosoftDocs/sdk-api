---
UID: NF:shobjidl_core.IFileSaveDialog.SetSaveAsItem
title: IFileSaveDialog::SetSaveAsItem
author: windows-sdk-content
description: Sets an item to be used as the initial entry in a Save As dialog.
old-location: shell\IFileSaveDialog_SetSaveAsItem.htm
tech.root: shell
ms.assetid: aa313685-1334-4899-a55a-6549b48e1464
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IFileSaveDialog interface [Windows Shell],SetSaveAsItem method, IFileSaveDialog.SetSaveAsItem, IFileSaveDialog::SetSaveAsItem, SetSaveAsItem, SetSaveAsItem method [Windows Shell], SetSaveAsItem method [Windows Shell],IFileSaveDialog interface, shell.IFileSaveDialog_SetSaveAsItem, shell_IFileSaveDialog_SetSaveAsItem, shobjidl_core/IFileSaveDialog::SetSaveAsItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
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
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog.SetSaveAsItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSaveDialog::SetSaveAsItem


## -description


Sets an item to be used as the initial entry in a <b>Save As</b> dialog.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The name of the item is displayed in the file name edit box, and the containing folder is opened in the view. This would generally be used when the application is saving an item that already exists. For new items, use <a href="https://msdn.microsoft.com/b8b72a76-6cdb-4675-8d84-f3c7171b8576">IFileDialog::SetFileName</a>.



