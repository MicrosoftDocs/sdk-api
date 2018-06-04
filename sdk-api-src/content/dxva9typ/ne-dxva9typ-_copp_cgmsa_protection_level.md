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

# _COPP_CGMSA_Protection_Level enumeration


## -description



Specifies the CGMS-A protection level.




## -enum-fields




### -field COPP_CGMSA_Disabled


            CGMS-A is disabled.
          


### -field COPP_CGMSA_LevelMin


            Minimum CGMS-A level. Equivalent to <b>COPP_CGMSA_Disabled</b>.
          


### -field COPP_CGMSA_CopyFreely


            The protection level is Copy Freely.
          


### -field COPP_CGMSA_CopyNoMore


            The protection level is Copy No More.
          


### -field COPP_CGMSA_CopyOneGeneration


            The protection level is Copy One Generation.
          


### -field COPP_CGMSA_CopyNever


            The protection level is Copy Never.
          


### -field COPP_CGMSA_RedistributionControlRequired

Redistribution control (or <i>broadcast flag</i>) is required. This flag can be combined with the other flags.


### -field COPP_CGMSA_LevelMax


            Maximum CGMS-A level.
          


### -field COPP_CGMSA_ForceDWORD


            Reserved.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

