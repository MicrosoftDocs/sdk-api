---
UID: NE:sensorsapi.LOCATION_DESIRED_ACCURACY
title: LOCATION_DESIRED_ACCURACY
author: windows-sdk-content
description: Defines the possible desired accuracy types.
old-location: winlocation\location_desired_accuracy.htm
tech.root: LocationAPI
ms.assetid: 5d3fc14b-fbf1-4140-8277-44e72a50e028
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LOCATION_DESIRED_ACCURACY, LOCATION_DESIRED_ACCURACY enumeration [WinLocation], LOCATION_DESIRED_ACCURACY_DEFAULT, LOCATION_DESIRED_ACCURACY_HIGH, sensorsapi/LOCATION_DESIRED_ACCURACY, sensorsapi/LOCATION_DESIRED_ACCURACY_DEFAULT, sensorsapi/LOCATION_DESIRED_ACCURACY_HIGH, winlocation.location_desired_accuracy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sensorsApi.h
api_name:
 - LOCATION_DESIRED_ACCURACY
product: Windows
targetos: Windows
req.typenames: LOCATION_DESIRED_ACCURACY
req.redist: 
---

# LOCATION_DESIRED_ACCURACY enumeration


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Defines the possible desired accuracy types.


## -enum-fields




### -field LOCATION_DESIRED_ACCURACY_DEFAULT

The sensor should use the accuracy for which it can optimize power use and other cost considerations.


### -field LOCATION_DESIRED_ACCURACY_HIGH

The sensor should deliver the most accurate report possible. This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.


## -see-also




<a href="https://msdn.microsoft.com/caa34e34-7370-4e42-9c0f-00498f5fc37d">GetDesiredAccuracy</a>



<a href="https://msdn.microsoft.com/85623570-3b48-42ea-babd-fe4282629d92">SetDesiredAccuracy</a>
 

 

