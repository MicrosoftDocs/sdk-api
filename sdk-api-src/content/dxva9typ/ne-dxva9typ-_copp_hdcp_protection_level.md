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

# _COPP_HDCP_Protection_Level enumeration


## -description



Specifies the HDCP protection level.




## -enum-fields




### -field COPP_HDCP_Level0


            HDCP protection is not enabled. See Remarks.
          


### -field COPP_HDCP_LevelMin


            Minimum HDCP level. Equivalent to <b>COPP_HDCP_Level0</b>.
          


### -field COPP_HDCP_Level1


            HDCP is enabled.
          


### -field COPP_HDCP_LevelMax


            Maximum HDCP level. Equivalent to <b>COPP_HDCP_Level1</b>.
          


### -field COPP_HDCP_ForceDWORD


            Reserved.
          


## -remarks



Some televisions do not have robust support for switching HDCP protection on and off. Because of this limitation, the graphics driver might leave HDCP enabled when the application sets the protection level to zero. If the application sets the HDCP level to zero, therefore, it might receive a COPP status message indicating that HDCP is still enabled. This is not an error.

For more information about HDCP, see <a href="http://go.microsoft.com/fwlink?linkID=161532">http://www.digital-cp.com/home</a>.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/23eebe93-416b-48c8-a05f-019e38b9a660">Using Certified Output Protection Protocol (COPP)</a>
 

 

