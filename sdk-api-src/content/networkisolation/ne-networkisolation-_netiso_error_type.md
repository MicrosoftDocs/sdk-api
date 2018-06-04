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

# _NETISO_ERROR_TYPE enumeration


## -description


The <b>NETISO_ERROR_TYPE</b> enumerated type specifies the type of error related to a network isolation operation.


## -enum-fields




### -field NETISO_ERROR_TYPE_NONE

No error.


### -field NETISO_ERROR_TYPE_PRIVATE_NETWORK

The failure was caused because the privateNetworkClientServer capability is missing.


### -field NETISO_ERROR_TYPE_INTERNET_CLIENT

The failure was caused because the internetClient capability is missing.


### -field NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER

The failure was caused because the internetClientServer capability is missing.


### -field NETISO_ERROR_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/fb59b2bb-03c1-472d-bb97-6fd9d5f7169d">NetworkIsolationDiagnoseConnectFailureAndGetInfo</a>
 

 

