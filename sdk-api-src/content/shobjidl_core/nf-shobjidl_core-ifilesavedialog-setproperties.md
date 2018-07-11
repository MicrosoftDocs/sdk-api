---
UID: NF:shobjidl_core.IFileSaveDialog.SetProperties
title: IFileSaveDialog::SetProperties
author: windows-sdk-content
description: Provides a property store that defines the default values to be used for the item being saved.
old-location: shell\IFileSaveDialog_SetProperties.htm
old-project: shell
ms.assetid: 418f2524-5e6d-4e79-894b-b5f706171836
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IFileSaveDialog interface [Windows Shell],SetProperties method, IFileSaveDialog.SetProperties, IFileSaveDialog::SetProperties, SetProperties, SetProperties method [Windows Shell], SetProperties method [Windows Shell],IFileSaveDialog interface, shell.IFileSaveDialog_SetProperties, shell_IFileSaveDialog_SetProperties, shobjidl_core/IFileSaveDialog::SetProperties
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
 - IFileSaveDialog.SetProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSaveDialog::SetProperties


## -description


Provides a property store that defines the default values to be used for the item being saved.


## -parameters




### -param pStore [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>*</b>

Pointer to the interface that represents the property store that contains the associated metadata.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be called at any time before the dialog is opened or while the dialog is showing. If an item has inherent properties, this method should be called with those properties before showing the dialog.

When using <b>Save As</b>, the application should provide the properites of the item being saved to the <b>Save</b> dialog. Those properties should be retreived from the original item by calling <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">GetPropertyStore</a> with the <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GPS_HANDLERPROPERTIESONLY</a> flag.

To retrieve the properties of the saved item (which may have been modified by the user) after the dialog closes, call <a href="https://msdn.microsoft.com/734a1bf9-ff63-48a5-9508-3a576ea24ab7">IFileSaveDialog::GetProperties</a>.

To turn on property collection and indicate which properties should be displayed in the <b>Save</b> dialog, use <a href="https://msdn.microsoft.com/cff40aba-6a87-4c20-957d-6729e0d995ae">IFileSaveDialog::SetCollectedProperties</a>.




## -see-also




<a href="https://msdn.microsoft.com/74021f92-54ff-4c02-a8cf-49bcd7b9171e">IFileSaveDialog</a>



<a href="https://msdn.microsoft.com/734a1bf9-ff63-48a5-9508-3a576ea24ab7">IFileSaveDialog::GetProperties</a>



<a href="https://msdn.microsoft.com/cff40aba-6a87-4c20-957d-6729e0d995ae">IFileSaveDialog::SetCollectedProperties</a>
 

 

