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

# Button_GetImageList macro


## -description


Gets the <a href="https://msdn.microsoft.com/c3a790ee-e247-47c1-9578-2b351cf725cd">BUTTON_IMAGELIST</a> structure that describes the image list that is set for a button control. You can use this macro or send the <a href="https://msdn.microsoft.com/79383758-53d4-4955-b472-befd338cbec6">BCM_GETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param pbuttonImagelist

TBD






#### - pbuttonImageList

Type: <b>PBUTTON_IMAGELIST</b>

A pointer to a <a href="https://msdn.microsoft.com/c3a790ee-e247-47c1-9578-2b351cf725cd">BUTTON_IMAGELIST</a> structure that contains image list information. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/79383758-53d4-4955-b472-befd338cbec6">BCM_GETIMAGELIST</a>



<a href="https://msdn.microsoft.com/c3a790ee-e247-47c1-9578-2b351cf725cd">BUTTON_IMAGELIST</a>



<b>Reference</b>
 

 

