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

# ListBox_GetItemHeight macro


## -description


Retrieves the height of items in a list box. If the list box has the <a href="List_Box_Styles.htm">LBS_OWNERDRAWVARIABLE</a> style, this macro gets the height of the specified item; otherwise, it gets the height of all items. You can use this macro or send the <a href="https://msdn.microsoft.com/ee96fce6-babd-4581-ac0e-2eb955fe543b">LB_GETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item. If the list box does not have the <a href="List_Box_Styles.htm">LBS_OWNERDRAWVARIABLE</a> style, set this parameter to zero. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/ee96fce6-babd-4581-ac0e-2eb955fe543b">LB_GETITEMHEIGHT</a>.
	



