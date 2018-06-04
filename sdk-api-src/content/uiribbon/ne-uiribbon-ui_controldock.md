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

# UI_CONTROLDOCK enumeration


## -description


Specifies values that identify the dock state of the Quick Access Toolbar (QAT). 


## -enum-fields




### -field UI_CONTROLDOCK_TOP

The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.

<img alt="Screen shot showing the Quick Access Toolbar docked above the Ribbon in the nonclient area." src="images/Properties/QAT_DockTop.png"/>


### -field UI_CONTROLDOCK_BOTTOM

The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.

<img alt="Screen shot showing the Quick Access Toolbar docked below the Ribbon." src="images/Properties/QAT_DockBottom.png"/>


## -remarks



The QAT dock position is based on the <b>UI_CONTROLDOCK</b> value in <a href="https://msdn.microsoft.com/77f7b0a8-f276-4501-9d53-fb5a3185edcc">UI_PKEY_QuickAccessToolbarDock</a>.




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/77f7b0a8-f276-4501-9d53-fb5a3185edcc">UI_PKEY_QuickAccessToolbarDock</a>
 

 

