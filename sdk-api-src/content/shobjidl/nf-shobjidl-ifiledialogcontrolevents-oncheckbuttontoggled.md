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

# IFileDialogControlEvents::OnCheckButtonToggled


## -description


Called when the user changes the state of a check button (check box).


## -parameters




### -param pfdc [in]

Type: <b><a href="https://msdn.microsoft.com/f1c29688-3538-40ff-a1da-6211cc5dded7">IFileDialogCustomize</a>*</b>

A pointer to the interface through which the application added controls to the dialog.


### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the button that the user clicked.


### -param bChecked [in]

Type: <b>BOOL</b>

A <b>BOOL</b> indicating the current state of the check button. <b>TRUE</b> if checked; <b>FALSE</b> otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



