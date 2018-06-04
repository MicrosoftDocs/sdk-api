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

# MonthCal_SetCalendarBorder macro


## -description


Sets the border size, in pixels, of a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/2a64a08f-a1fb-47a8-8f09-725807e87a03">MCM_SETCALENDARBORDER</a> message explicitly.


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control.


### -param fset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, then the border size is set to the number of pixels that <i>xyborder</i> specifies. If <b>FALSE</b>, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.


### -param xyborder

Type: <b>int</b>

Number of pixels of the border size.

