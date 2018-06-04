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

# _CRYPT_TIMESTAMP_ACCURACY structure


## -description


The <b>CRYPT_TIMESTAMP_ACCURACY</b> structure is used by the <a href="https://msdn.microsoft.com/05ca0877-5e9d-4b21-9fca-a1eef2cb4626">CRYPT_TIMESTAMP_INFO</a> structure to represent the accuracy of the time deviation around the UTC time at which the time stamp token was created by the Time Stamp Authority (TSA).


## -struct-fields




### -field dwSeconds

Optional. Specifies, in seconds, the accuracy of the upper limit of the time at which the time stamp token was created by the TSA.


### -field dwMillis

Optional. Specifies, in milliseconds, the accuracy of the upper limit of the time at which the time stamp token was  created by the TSA.


### -field dwMicros

Optional. Specifies, in microseconds, the accuracy of the upper limit of the time at which the time-stamp token was created by the TSA.

