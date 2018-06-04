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

# IGPMClientSideExtension::IsComputerEnabled


## -description


Checks whether the client-side extension can be called during the processing of computer policy.


## -parameters




### -param pvbEnabled [out]

Value that indicates whether the client-side extension can be called during the processing of computer policy. If <b>VARIANT_TRUE</b>, the client-side extension is called during the processing of computer policy, provided that there are policy settings for the client-side extension in the computer portion of one or more of the applied GPOs.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the client-side extension can be configured in the computer portion of the GPO. If <b>VARIANT_TRUE</b>, the client-side extension can be configured.

<h3>VB</h3>
Value that indicates whether the client-side extension can be configured in the computer portion of the GPO. If <b>VARIANT_TRUE</b>, the client-side extension can be configured.




## -see-also




<a href="https://msdn.microsoft.com/b29f4d09-60c0-4c67-b295-05c7d9a05397">IGPMClientSideExtension</a>
 

 

