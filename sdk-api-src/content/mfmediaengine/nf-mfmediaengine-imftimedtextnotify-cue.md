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

# IMFTimedTextNotify::Cue


## -description


Called when a cue event occurs in a text track.


## -parameters




### -param cueEvent [in]

Type: <b><a href="https://msdn.microsoft.com/8EA769FD-8BA9-4EBA-96AE-C86720A5F1F1">MF_TIMED_TEXT_CUE_EVENT</a></b>

A value specifying the type of event that has occured.


### -param currentTime [in]

Type: <b>double</b>

The current time when the cue event occurred.


### -param cue






#### - pCue [in]

Type: <b><a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>*</b>

The <a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a> object representing the cue.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/FE782D90-8CD4-4F8B-A20E-CE3F792A2DB4">IMFTimedTextNotify</a>
 

 

