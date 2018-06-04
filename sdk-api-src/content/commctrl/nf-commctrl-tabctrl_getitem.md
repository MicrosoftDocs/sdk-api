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

# TabCtrl_GetItem macro


## -description


Retrieves information about a tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/41774f14-c4e9-4c98-bc25-3522b2125ed5">TCM_GETITEM</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param iItem

Type: <b>int</b>

Index of the tab. 


### -param pitem

Type: <b>LPTCITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/e08c4528-5874-492c-97be-dfdf5f5636a9">TCITEM</a> structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the 
					<b>mask</b> member specifies which attributes to return. If the <b>mask</b> member specifies the TCIF_TEXT value, the 
<b>pszText</b> member must contain the address of the buffer that receives the item text, and the <b>cchTextMax</b> member must specify the size of the buffer.


## -remarks



If the TCIF_TEXT flag is set in the 
				<b>mask</b> member of the <a href="https://msdn.microsoft.com/e08c4528-5874-492c-97be-dfdf5f5636a9">TCITEM</a> structure, the control may change the <b>pszText</b> member of the structure to point to the new text instead of filling the buffer with the requested text. The control may set the <b>pszText</b> member to <b>NULL</b> to indicate that no text is associated with the item.



