---
UID: NF:shobjidl_core.IFileOperation.SetProgressDialog
title: IFileOperation::SetProgressDialog
author: windows-sdk-content
description: Specifies a dialog box used to display the progress of the operation.
old-location: shell\IFileOperation_SetProgressDialog.htm
tech.root: Shell
ms.assetid: 34cc6b88-9791-4778-a8d9-cf1b80aa42a8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IFileOperation interface [Windows Shell],SetProgressDialog method, IFileOperation.SetProgressDialog, IFileOperation::SetProgressDialog, SetProgressDialog, SetProgressDialog method [Windows Shell], SetProgressDialog method [Windows Shell],IFileOperation interface, _shell_IFileOperation_SetProgressDialog, shell.IFileOperation_SetProgressDialog, shobjidl_core/IFileOperation::SetProgressDialog
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
 - IFileOperation.SetProgressDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperation::SetProgressDialog


## -description


Specifies a dialog box used to display the progress of the operation.


## -parameters




### -param popd [in]

Type: <b><a href="https://msdn.microsoft.com/0d95f407-0e09-441d-b9e2-665995ea1362">IOperationsProgressDialog</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/0d95f407-0e09-441d-b9e2-665995ea1362">IOperationsProgressDialog</a> object that represents the dialog box.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



