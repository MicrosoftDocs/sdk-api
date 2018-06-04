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

# IFileDialogControlEvents::OnItemSelected


## -description


Called when an item is selected in a combo box, when a user clicks an option button (also known as a radio button), or an item is chosen from the <b>Tools</b> menu.


## -parameters




### -param pfdc [in]

Type: <b><a href="https://msdn.microsoft.com/f1c29688-3538-40ff-a1da-6211cc5dded7">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.


### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control in which the user made a selection.


### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the selection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This notification is not sent when the user chooses an item from the drop-down menu attached to the <b>Open</b> button, because the action taken in that case is always the same: close the dialog as if the user had simply clicked the <b>Open</b> button. For that situation, the application can call <a href="https://msdn.microsoft.com/1dd33779-071f-484e-9d89-1cc64ea03293">GetSelectedControlItem</a> to obtain the item the user chose from that menu.



