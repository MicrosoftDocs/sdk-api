---
UID: NS:ras._RAS_PROJECTION_INFO
title: "_RAS_PROJECTION_INFO"
author: windows-sdk-content
description: Contains the Point-to-Point (PPP) or Internet Key Exchange version 2 (IKEv2) projection information for a RAS connection.
old-location: rras\ras_projection_info.htm
old-project: rras
ms.assetid: ca4fbaff-f035-4340-8d29-7dcddaf1b1bb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PRAS_PROJECTION_INFO, PRAS_PROJECTION_INFO, PRAS_PROJECTION_INFO structure pointer [RAS], RAS_PROJECTION_INFO, RAS_PROJECTION_INFO structure [RAS], _RAS_PROJECTION_INFO, ras/PRAS_PROJECTION_INFO, ras/RAS_PROJECTION_INFO, rras.ras_projection_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RAS_PROJECTION_INFO, *PRAS_PROJECTION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ras.h
api_name:
 - RAS_PROJECTION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

