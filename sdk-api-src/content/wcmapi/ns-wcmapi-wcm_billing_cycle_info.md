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

# WCM_BILLING_CYCLE_INFO structure


## -description


The <b>WCM_BILLING_CYCLE_INFO</b> structure specifies information about the billing cycle.


## -struct-fields




### -field StartDate

Type: <b>FILETIME</b>

Specifies the start date of the cycle.


### -field Duration

Type: <b><a href="https://msdn.microsoft.com/7744a577-5f3d-4cdd-b74d-a1430ea20b37">WCM_TIME_INTERVAL</a></b>

Specifies the billing cycle duration.


### -field Reset

Type: <b>BOOL</b>

True if at the end of the billing cycle, a new billing cycle of the same duration will start. False if the service will terminate at the end of the billing cycle.


## -see-also




<a href="https://msdn.microsoft.com/7744a577-5f3d-4cdd-b74d-a1430ea20b37">WCM_TIME_INTERVAL</a>
 

 

