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

# _RAS_PROJECTION_INFO structure


## -description


The <b>RAS_PROJECTION_INFO</b> structure contains the  Point-to-Point (PPP) or Internet Key Exchange version 2 (IKEv2) projection information for a RAS connection.


## -struct-fields




### -field version

A <a href="https://msdn.microsoft.com/da0026a3-0ccc-46aa-a62e-3d334c5bfe11">RASAPIVERSION</a> value that specifies the structure version.


### -field type

A <a href="https://msdn.microsoft.com/ac288100-a346-4d9b-9bf4-8144372f54a3">RASPROJECTION_INFO_TYPE</a> value that specifies the connection type in <b>union</b>.


### -field ppp

 


### -field ikev2

 




#### - union



#### ppp

A <a href="https://msdn.microsoft.com/8394b843-75f0-4bbd-9ad8-6f4b5dc4bf7b">RASPPP_PROJECTION_INFO</a> structure that contains the PPP projection information of a RAS connection.



#### ikev2

A <a href="https://msdn.microsoft.com/c88346f0-118e-4468-83b1-2dfc263e22f7">RASIKEV2_PROJECTION_INFO</a> structure that contains the IKEv2 projection information of a RAS connection.


## -see-also




<a href="https://msdn.microsoft.com/e34216ed-fa78-4cb3-8db9-274c8ba196dd">RasGetProjectionInfoEx</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/c20e8892-7c5e-48cc-939a-9b747fefe09d">Remote Access Service Structures</a>
 

 

