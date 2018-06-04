---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

