---
UID: NF:shobjidl_core.IFileSaveDialog.ApplyProperties
title: IFileSaveDialog::ApplyProperties
author: windows-sdk-content
description: Applies a set of properties to an item using the Shell's copy engine.
old-location: shell\IFileSaveDialog_ApplyProperties.htm
old-project: shell
ms.assetid: 3de64914-b64e-47e8-8f84-6c64d849ffa9
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: ApplyProperties, ApplyProperties method [Windows Shell], ApplyProperties method [Windows Shell],IFileSaveDialog interface, IFileSaveDialog interface [Windows Shell],ApplyProperties method, IFileSaveDialog.ApplyProperties, IFileSaveDialog::ApplyProperties, shell.IFileSaveDialog_ApplyProperties, shell_IFileSaveDialog_ApplyProperties, shobjidl_core/IFileSaveDialog::ApplyProperties
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog.ApplyProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSaveDialog::ApplyProperties


## -description


Applies a set of properties to an item using the Shell's copy engine.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the file being saved. This is usually the item retrieved by <a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">GetResult</a>.


### -param pStore [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> that represents the property values to be applied to the file. This can be the property store returned by <a href="https://msdn.microsoft.com/734a1bf9-ff63-48a5-9508-3a576ea24ab7">IFileSaveDialog::GetProperties</a>.


### -param hwnd [in]

Type: <b>HWND</b>

The handle of the application window.


### -param pSink [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an optional <b>IFileOperationProgressSink</b> that the calling application can use if they want to be notified of the progress of the property stamping. This value may be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should be used when the application has turned on property collection (<a href="https://msdn.microsoft.com/cff40aba-6a87-4c20-957d-6729e0d995ae">IFileSaveDialog::SetCollectedProperties</a>), but does not persist the properties themselves into the saved file.

<div class="alert"><b>Note</b>  The file represented by the item specified in <i>psi</i> must exist in physical storage before making the call to <b>IFileSaveDialog::ApplyProperties</b>, so it must have been previously saved at some point.</div>
<div> </div>


