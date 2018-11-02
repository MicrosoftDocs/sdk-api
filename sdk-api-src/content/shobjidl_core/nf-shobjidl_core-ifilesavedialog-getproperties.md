---
UID: NF:shobjidl_core.IFileSaveDialog.GetProperties
title: IFileSaveDialog::GetProperties
author: windows-sdk-content
description: Retrieves the set of property values for a saved item or an item in the process of being saved.
old-location: shell\IFileSaveDialog_GetProperties.htm
tech.root: shell
ms.assetid: 734a1bf9-ff63-48a5-9508-3a576ea24ab7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetProperties, GetProperties method [Windows Shell], GetProperties method [Windows Shell],IFileSaveDialog interface, IFileSaveDialog interface [Windows Shell],GetProperties method, IFileSaveDialog.GetProperties, IFileSaveDialog::GetProperties, shell.IFileSaveDialog_GetProperties, shell_IFileSaveDialog_GetProperties, shobjidl_core/IFileSaveDialog::GetProperties
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
 - IFileSaveDialog.GetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSaveDialog::GetProperties


## -description


Retrieves the set of property values for a saved item or an item in the process of being saved.


## -parameters




### -param ppStore

TBD




#### - pStore [out]

Type: <b><a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> that receives the property values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be called while the dialog is showing to retrieve the current set of values in the metadata collection pane. It can also be called after the dialog has closed, to retrieve the final set of values.

The call to this method will fail unless property collection has been turned on with a call to <a href="https://msdn.microsoft.com/cff40aba-6a87-4c20-957d-6729e0d995ae">IFileSaveDialog::SetCollectedProperties</a>.



