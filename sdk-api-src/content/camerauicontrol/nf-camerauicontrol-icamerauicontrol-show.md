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

# ICameraUIControl::Show


## -description


Displays the user interface control for the camera.


## -parameters




### -param pWindow [in]

Pointer to the user interface window.


### -param mode [in]

Specifies whether the user interface will be presented in a browseable or linear manner.


### -param selectionMode




### -param captureMode [in]

Specifies whether the user interface that will be shown allows the user to capture a photo, capture a video, or either.


### -param photoFormat [in]

Provides the format for capturing photos. The available formats include JPEG, PNG, and JPEG XR.


### -param videoFormat [in]

Provides the format for capturing videos. The available formats include MP4 and WMV.


### -param bHasCloseButton [in]

TRUE if the user interface has a close button, otherwise, FALSE.


### -param pEventCallback [in]

Pointer to an event callback for the dialog. The callback is invoked if an item is captured or deleted, and when the dialog starts, or is closed or suspended.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e0fbcf43-cd52-4b5b-af4b-f7d673f7a7c9">ICameraUIControl</a>
 

 

