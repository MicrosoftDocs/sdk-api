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

# DateTime_GetRange macro


## -description


Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro, or send the <a href="https://msdn.microsoft.com/190cada6-49ee-483f-a464-d3d789127159">DTM_GETRANGE</a> message explicitly. 


## -parameters




### -param hdp

TBD


### -param rgst

TBD






#### - hwndDT

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control.


#### - lpSysTimeArray

Type: <b>LPSYSTEMTIME</b>

A pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures. 


## -remarks



The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range. If the <a href="https://msdn.microsoft.com/9ac12f31-09d8-4220-939c-24fbb92cb6ed">DateTime_SetSystemtime</a> message specifies a date and time that falls outside the range, it will fail.



