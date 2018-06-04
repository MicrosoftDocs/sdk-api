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

# _DWM_PRESENT_PARAMETERS structure


## -description


Specifies Desktop Window Manager (DWM) video frame parameters for frame composition. Used by the <a href="https://msdn.microsoft.com/75684283-9e5e-4c17-b642-7c309a389f6f">DwmSetPresentParameters</a> function.


## -struct-fields




### -field cbSize

The size of the <b>DWM_PRESENT_PARAMETERS</b> structure.


### -field fQueue

<b>TRUE</b> if the caller is requesting queued presents; otherwise, <b>FALSE</b>. If <b>TRUE</b>, the remaining parameters must be specified. If <b>FALSE</b>, queued presentation is disabled for this window and present behavior returns to the default behavior.


### -field cRefreshStart

A <b>ULONGLONG</b> value that provides the refresh number that the next presented frame should begin to display.


### -field cBuffer

The number of frames the application is instructing DWM to queue. The valid range is 2-8.


### -field fUseSourceRate

<b>TRUE</b> if the application wants DWM to schedule presentation based on source rate. <b>FALSE</b> if the application will decide how many refreshes to display for each frame. If <b>TRUE</b>, <b>rateSource</b> must be specified. If <b>FALSE</b>, <b>cRefreshesPerFrame</b> must be specified.


### -field rateSource

The rate, in frames per second, of the source material being displayed.


### -field cRefreshesPerFrame

The number of monitor refreshes through which each frame should be displayed on the screen.


### -field eSampling

The frame sampling type to use for composition.


## -remarks



The <b>rateSource</b> member is expressed as a ratio so that content (like that using NTSC standards, which has a rate of 60000/1001) can be accurately expressed. DWM determines how long to display each frame by resampling between the source rate and the composition rate in use each time the desktop is composed.



