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

# DWMFLIP3DWINDOWPOLICY enumeration


## -description


Flags used by the <a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a> function to specify the Flip3D window policy.


## -enum-fields




### -field DWMFLIP3D_DEFAULT

Use the window's style and visibility settings to determine whether to hide or include the window in Flip3D rendering.


### -field DWMFLIP3D_EXCLUDEBELOW

Exclude the window from Flip3D and display it below the Flip3D rendering.


### -field DWMFLIP3D_EXCLUDEABOVE

Exclude the window from Flip3D and display it above the Flip3D rendering.


### -field DWMFLIP3D_LAST

The maximum recognized <a href="https://msdn.microsoft.com/48dae43d-f184-4665-aada-7539559ecfe5">DWMFLIP3DWINDOWPOLICY</a> value, used for validation purposes.


## -remarks



To use a <b>DWMFLIP3DWINDOWPOLICY</b> value, set the <i>dwAttribute</i> parameter of the <a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a> function to <b>DWMWA_FLIP3D_POLICY</b>. Set the <i>pvAttribute</i> parameter to the <b>DWMFLIP3DWINDOWPOLICY</b> value.




## -see-also




<a href="https://msdn.microsoft.com/b728db22-db83-4607-8b09-6967697ef1b0">Enable and Control DWM Composition</a>
 

 

