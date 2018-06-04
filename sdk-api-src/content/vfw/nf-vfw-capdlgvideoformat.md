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

# capDlgVideoFormat macro


## -description



The <b>capDlgVideoFormat</b> macro displays a dialog box in which the user can select the video format. The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/3b44507e-3806-467f-877a-e9992d1337cb">WM_CAP_DLG_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



After this message returns, applications might need to update the <a href="https://msdn.microsoft.com/65ad6e33-c601-4026-a5a4-2c68576d7ab7">CAPSTATUS</a> structure because the user might have changed the image dimensions.

The Video Format dialog box is unique for each capture driver. Some capture drivers might not support a Video Format dialog box. Applications can determine if the capture driver supports this message by checking the <b>fHasDlgVideoFormat</b> member of <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a>.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

