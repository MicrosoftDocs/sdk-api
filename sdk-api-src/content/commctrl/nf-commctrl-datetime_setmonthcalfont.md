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

# DateTime_SetMonthCalFont macro


## -description


Sets the font to be used by the date and time picker (DTP) control's child month calendar control. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/5033e975-9b68-438a-99c3-80ca02cd59e7">DTM_SETMCFONT</a> message. 


## -parameters




### -param hdp

TBD


### -param hfont

TBD


### -param fRedraw

Type: <b>long</b>

Specifies whether the control should be redrawn immediately upon setting the font. Setting this parameter to <b>TRUE</b> causes the control to redraw itself. 


#### - hFont

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HFONT</a></b>

A handle to the font that will be set. 


#### - hwndDP

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 

