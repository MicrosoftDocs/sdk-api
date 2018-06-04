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

# WdsCliObtainDriverPackages function


## -description


This function obtains from a WDS image, the driver packages (INF files) that can be used on this computer. The <a href="https://msdn.microsoft.com/37d96077-d3f0-4372-955d-f8c071d82230">WdsCliFreeStringArray</a> function can be used to free the array of string values allocated by this function. 


## -parameters




### -param hImage [in]

A handle to a WDS image.


### -param ppwszServerName [out]

A pointer to a pointer to a string value that receives the IP address of the server hosting the driver packages.


### -param pppwszDriverPackages [out]

An array of string values that are the full paths for the driver packages (INF files.) The Internet Protocol (IP) address, rather than a computer name, is returned as part of the path.  For example, a string value <b>\\172.31.224.245\REMINST\Stores\Drivers\driver.inf</b> in the array gives the full path to driver.inf.

<div class="code"></div>

### -param pulCount [out]

The number of driver packages returned by <i>pppwszDriverPackages</i>.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

