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

# ComboBox_SetItemHeight macro


## -description


Sets the height of list items or the selection field in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/25a01170-5ffc-4d86-b696-706f5375570b">CB_SETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The component of the combo box for which to set the height. This parameter must be –1 to set the height of the selection field. It must be zero to set the height of list items, unless the combo box has the <a href="Combo_Box_Styles.htm">CBS_OWNERDRAWVARIABLE</a> style. In that case, the <i>index</i> parameter is the zero-based index of a specific list item.


### -param cyItem

Type: <b>int</b>

The height in pixels.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/25a01170-5ffc-4d86-b696-706f5375570b">CB_SETITEMHEIGHT</a>.
	



