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

# WICGifGraphicControlExtensionProperties enumeration


## -description


Specifies the graphic control extension metadata properties that define the transitions between each frame animation for Graphics Interchange Format (GIF) images.


## -enum-fields




### -field WICGifGraphicControlExtensionDisposal

[VT_UI1] Indicates  the disposal requirements. 0 - no disposal, 1 - do not dispose, 2 - restore to background color, 3 - restore to previous.


### -field WICGifGraphicControlExtensionUserInputFlag

[VT_BOOL] Indicates the user input flag. <b>TRUE</b> if user input should advance to the next frame; otherwise, <b>FALSE</b>.


### -field WICGifGraphicControlExtensionTransparencyFlag

[VT_BOOL] Indicates the transparency flag. <b>TRUE</b> if a transparent color in is in the color table for this frame; otherwise, <b>FALSE</b>.


### -field WICGifGraphicControlExtensionDelay

[VT_UI2] Indicates  how long to display the next frame before advancing to the next frame, in units of 1/100th of a second.


### -field WICGifGraphicControlExtensionTransparentColorIndex

[VT_UI1] Indicates which color in the palette should be treated as transparent.


### -field WICGifGraphicControlExtensionProperties_FORCE_DWORD



