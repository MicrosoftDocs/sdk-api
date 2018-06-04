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

# ListView_SetCheckState macro


## -description


Selects or deselects an item in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/aecd14dd-cfd0-4c7c-bddc-f65022de68c9">LVM_SETITEMSTATE</a> message explicitly.


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param i

TBD


### -param fCheck

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value that is set to <b>TRUE</b> to select the item, or <b>FALSE</b> to deselect it. 


#### - iIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the item for which to set the check state. 


## -remarks



This macro should only be used for list-view controls with the <a href="Extended_list_view_styles.htm">LVS_EX_CHECKBOXES</a> style. 




## -see-also




<a href="https://msdn.microsoft.com/b90900f1-833b-418c-8ddc-76c0743b77f9">ListView_SetItemState</a>
 

 

