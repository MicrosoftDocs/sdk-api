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

# UnregisterAuthoringClientFunctionType callback function


## -description


Unregisters the application-defined function that was registered with the <a href="https://msdn.microsoft.com/31414CBA-12A3-45F8-967B-7ECD9D90D0F6">RegisterAuthoringClientFunctionType</a> function. This function is called when the app host  terminates.


## -parameters




### -param *host [in]

Type: <b><a href="https://msdn.microsoft.com/ac0ace8e-3f83-44be-baee-560c5472aa08">IWebApplicationHost</a>*</b>

An object that provides a path to the authoring binary.


## -returns



Type: <b>HRESULT</b>

The WWAHost.




## -see-also




<a href="https://msdn.microsoft.com/31414CBA-12A3-45F8-967B-7ECD9D90D0F6">RegisterAuthoringClientFunctionType</a>
 

 

