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

# LsaNtStatusToWinError function


## -description


The <b>LsaNtStatusToWinError</b> function converts an NTSTATUS code returned by an LSA function to a Windows error code.


## -parameters




### -param Status [in]

An NTSTATUS code returned by an LSA function call. This value will be converted to a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System error code</a>.


## -returns



The return value is the Windows error code that corresponds to the <i>Status</i> parameter. If there is no corresponding Windows error code, the return value is ERROR_MR_MID_NOT_FOUND.




## -see-also




<a href="management_return_values.htm">LSA Policy Function Return Values</a>
 

 

