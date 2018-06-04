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

# IMenuPopup::OnSelect


## -description


Handles selection notifications.


## -parameters




### -param dwSelectType

Type: <b>DWORD</b>

This parameter can be any of the following values.



#### MPOS_EXECUTE

Execute the selected menu item.



#### MPOS_FULLCANCEL

Cancel the entire menu.



#### MPOS_CANCELLEVEL

Cancel the current cascaded menu.



#### MPOS_SELECTLEFT

Select the item to the left of the current selection.



#### MPOS_SELECTRIGHT

Select the item to the right of the current selection.



#### MPOS_CHILDTRACKING

The child of the current selection receives a tracking selection. In other words, the mouse moves over the child of the current selection.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.



