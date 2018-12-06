---
UID: NF:shobjidl_core.IFileDialog.Advise
title: IFileDialog::Advise
author: windows-sdk-content
description: Assigns an event handler that listens for events coming from the dialog.
old-location: shell\IFileDialog_Advise.htm
tech.root: shell
ms.assetid: f5664a52-f26c-475d-84ef-0c657ae46e2e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],Advise method, IFileDialog.Advise, IFileDialog::Advise, shell.IFileDialog_Advise, shell_IFileDialog_Advise, shobjidl_core/IFileDialog::Advise
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
 - IFileDialog.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialog::Advise


## -description


Assigns an event handler that listens for events coming from the dialog.


## -parameters




### -param pfde [in]

Type: <b><a href="https://msdn.microsoft.com/c55107a3-ae0a-4b46-80a3-8a731b47976c">IFileDialogEvents</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c55107a3-ae0a-4b46-80a3-8a731b47976c">IFileDialogEvents</a> implementation that will receive events from the dialog.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> that receives a value identiying this event handler. When the client is finished with the dialog, that client must call the <a href="https://msdn.microsoft.com/48504141-6612-43fe-8470-a9871b560f1a">IFileDialog::Unadvise</a> method with this value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



