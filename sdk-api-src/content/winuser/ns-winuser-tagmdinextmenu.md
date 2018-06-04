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

# tagMDINEXTMENU structure


## -description


Contains information about the menu to be activated. 


## -struct-fields




### -field hmenuIn

Type: <b>HMENU</b>

A handle to the current menu. 


### -field hmenuNext

Type: <b>HMENU</b>

A handle to the menu to be activated. 


### -field hwndNext

Type: <b>HWND</b>

A handle to the window to receive the menu notification messages. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6">WM_NEXTMENU</a>
 

 

