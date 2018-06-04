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

# tagRASDEVSPECIFICINFO structure


## -description


The <b>RASDEVSPECIFICINFO</b> structure is used to send a cookie for server validation and bypass point-to-point (PPP) authentication.


## -struct-fields




### -field dwSize

The size, in bytes, of the cookie in <b>pbDevSpecificInfo</b>.


### -field pbDevSpecificInfo

A pointer to a BLOB that contains the authentication cookie.


## -see-also




<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/c20e8892-7c5e-48cc-939a-9b747fefe09d">Remote Access Service Structures</a>
 

 

