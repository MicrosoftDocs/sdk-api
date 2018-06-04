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

# _DWM_BLURBEHIND structure


## -description


Specifies Desktop Window Manager (DWM) blur-behind properties. Used by the <a href="https://msdn.microsoft.com/e4b99f11-cab0-4713-8112-aab93c78378d">DwmEnableBlurBehindWindow</a> function.


## -struct-fields




### -field dwFlags

A bitwise combination of <a href="https://msdn.microsoft.com/d6dd552c-1f3b-4f16-8705-f5016ed55d9e">DWM Blur Behind</a> constant values that indicates which of the members of this structure have been set.


### -field fEnable

<b>TRUE</b> to register the window handle to DWM blur behind; <b>FALSE</b> to unregister the window handle from DWM blur behind.


### -field hRgnBlur

The region within the client area where the blur behind will be applied. A <b>NULL</b> value will apply the blur behind the entire client area.


### -field fTransitionOnMaximized

<b>TRUE</b> if the window's colorization should transition to match the maximized windows; otherwise, <b>FALSE</b>.

