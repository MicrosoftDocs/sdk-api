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

# THUMBBUTTONFLAGS enumeration


## -description


Used by <a href="https://msdn.microsoft.com/c13657b2-5b96-45ae-b339-b06b13aca65d">THUMBBUTTON</a> to control specific states and behaviors of the button.


## -enum-fields




### -field THBF_ENABLED

The button is active and available to the user.


### -field THBF_DISABLED

The button is disabled. It is present, but has a visual state that indicates that it will not respond to user action.


### -field THBF_DISMISSONCLICK

When the button is clicked, the taskbar button's flyout closes immediately.


### -field THBF_NOBACKGROUND

Do not draw a button border, use only the image.


### -field THBF_HIDDEN

The button is not shown to the user.


### -field THBF_NONINTERACTIVE

The button is enabled but not interactive; no pressed button state is drawn. This value is intended for instances where the button is used in a notification.


## -see-also




<a href="https://msdn.microsoft.com/c13657b2-5b96-45ae-b339-b06b13aca65d">THUMBBUTTON</a>



<a href="https://msdn.microsoft.com/12c6a535-6a23-4b41-b4fd-4ed4e192d629">THUMBBUTTONMASK</a>
 

 

