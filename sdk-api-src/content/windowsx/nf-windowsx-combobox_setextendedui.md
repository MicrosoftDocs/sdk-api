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

# ComboBox_SetExtendedUI macro


## -description


Selects either the default user interface (UI) or the extended UI for a combo box that has the <a href="Combo_Box_Styles.htm">CBS_DROPDOWN</a> or <a href="Combo_Box_Styles.htm">CBS_DROPDOWNLIST</a> style. You can use this macro or send the <a href="https://msdn.microsoft.com/c489e484-777e-4afa-996b-1ec3eb6552ab">CB_SETEXTENDEDUI</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero to use the default UI, or nonzero to use the extended UI.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/c489e484-777e-4afa-996b-1ec3eb6552ab">CB_SETEXTENDEDUI</a>.
	



