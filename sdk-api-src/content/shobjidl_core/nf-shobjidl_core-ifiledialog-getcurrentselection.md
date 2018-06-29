---
UID: NF:shobjidl_core.IFileDialog.GetCurrentSelection
title: IFileDialog::GetCurrentSelection
author: windows-sdk-content
description: Gets the user's current selection in the dialog.
old-location: shell\IFileDialog_GetCurrentSelection.htm
old-project: shell
ms.assetid: b3768c15-d933-43c0-8398-f8f1c16ecbf9
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetCurrentSelection, GetCurrentSelection method [Windows Shell], GetCurrentSelection method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],GetCurrentSelection method, IFileDialog.GetCurrentSelection, IFileDialog::GetCurrentSelection, shell.IFileDialog_GetCurrentSelection, shell_IFileDialog_GetCurrentSelection, shobjidl_core/IFileDialog::GetCurrentSelection
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialog.GetCurrentSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::GetCurrentSelection


## -description


Gets the user's current selection in the dialog.


## -parameters




### -param ppsi [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The address of a pointer to the interface that represents the item currently selected in the dialog. This item can be a file or folder selected in the view window, or something that the user has entered into the dialog's edit box. The latter case may require a parsing operation (cancelable by the user) that blocks the current thread.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




              The calling application is responsible for releasing the retrieved <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> when it is no longer needed.
            




## -see-also




<a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>



<a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">IFileDialog::GetResult</a>
 

 

