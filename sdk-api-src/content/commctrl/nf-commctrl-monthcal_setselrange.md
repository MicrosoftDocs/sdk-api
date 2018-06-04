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

# MonthCal_SetSelRange macro


## -description


Sets the selection for a month calendar control to a given date range. You can use this macro or send the <a href="https://msdn.microsoft.com/750b0c83-6baa-4caa-a738-feae8751a70e">MCM_SETSELRANGE</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param rgst

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lprgSysTimeArray

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures that contain date information representing the selection limits. The first selected date must be specified in <i>lprgSysTimeArray</i>[0], and the last selected date must be specified in <i>lprgSysTimeArray</i>[1]. The time members of these structures are ignored. 

