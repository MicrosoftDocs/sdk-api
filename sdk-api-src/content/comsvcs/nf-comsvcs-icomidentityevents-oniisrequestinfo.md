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

# IComIdentityEvents::OnIISRequestInfo


## -description


Generated when an activity is part of an ASP page.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ObjId [in]

The unique identifier for this object.


### -param pszClientIP [in]

The Internet Protocol (IP) address of the IIS client.


### -param pszServerIP [in]

The IP address of the IIS server.


### -param pszURL [in]

The URL on IIS server generating object reference.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f064a5cd-c84d-4b80-96fc-1036af333901">IComIdentityEvents</a>
 

 

