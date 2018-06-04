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

# WdsCliFreeStringArray function


## -description


This function can be used to free the array of string values that gets allocated by the <a href="https://msdn.microsoft.com/2fb6bf5a-a46f-4664-be0a-6b4f2563986c">WdsCliObtainDriverPackages</a> function. 


## -parameters




### -param ppwszArray [in, out, optional]

Pointer to the array of string values being freed.


### -param ulCount [in]

Number of strings in the array that is pointed to by <i>ppwszArray</i>.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



