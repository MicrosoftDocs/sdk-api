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

# _MI_Datetime structure


## -description


Represents a union of <a href="https://msdn.microsoft.com/f06f1b0e-d21c-4b60-8099-222a1582fde1">MI_Timestamp</a> and <a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>.


## -struct-fields




### -field isTimestamp

If <b>isTimestamp</b> is nonzero, timestamp is used.  If <b>isTimestamp</b> is 0, interval is used.


### -field u


### -field u.timestamp

If <b>isTimestamp</b> is nonzero, <b>MI_Datetime</b> is used to represent an absolute date/time.


### -field u.interval

If <b>isTimestamp</b> is nonzero,  <b>MI_Datetime</b> is used to represent a relative date/time from when it is needed.

