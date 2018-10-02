---
UID: NF:shobjidl_core.IFileOpenDialog.GetResults
title: IFileOpenDialog::GetResults
author: windows-sdk-content
description: Gets the user's choices in a dialog that allows multiple selection.
old-location: shell\IFileOpenDialog_GetResults.htm
tech.root: Shell
ms.assetid: 5c710dae-4988-4f19-beb5-2ff9cd11c596
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetResults, GetResults method [Windows Shell], GetResults method [Windows Shell],IFileOpenDialog interface, IFileOpenDialog interface [Windows Shell],GetResults method, IFileOpenDialog.GetResults, IFileOpenDialog::GetResults, shell.IFileOpenDialog_GetResults, shell_IFileOpenDialog_GetResults, shobjidl_core/IFileOpenDialog::GetResults
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
 - IFileOpenDialog.GetResults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOpenDialog::GetResults


## -description


Gets the user's choices in a dialog that allows multiple selection.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>**</b>

The address of a pointer to an <b>IShellItemArray</b> through which the items selected in the dialog can be accessed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be used whether the selection consists of a single item or multiple items.

<b>IFileOpenDialog::GetResult</b> can be called after the dialog has closed or during the handling of an IFileDialogEvents::OnFileOk event. Calling this method at any other time will fail.


<a href="https://msdn.microsoft.com/0284b694-64d1-48db-bef3-92f808b29b23">Show</a> must return a success code for a result to be available to <b>IFileOpenDialog::GetResult</b>.



