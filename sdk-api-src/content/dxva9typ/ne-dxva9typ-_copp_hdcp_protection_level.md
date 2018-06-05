---
UID: NE:dxva9typ._COPP_HDCP_Protection_Level
title: "_COPP_HDCP_Protection_Level"
author: windows-sdk-content
description: Specifies the HDCP protection level.
old-location: dshow\copp_hdcp_protection_level.htm
old-project: DirectShow
ms.assetid: 902ea4c6-8eba-4bfd-b986-5e7a5a2a5971
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: COPP_HDCP_ForceDWORD, COPP_HDCP_Level0, COPP_HDCP_Level1, COPP_HDCP_LevelMax, COPP_HDCP_LevelMin, COPP_HDCP_Protection_Level, COPP_HDCP_Protection_Level , COPP_HDCP_Protection_Level enumeration [DirectShow], COPP_HDCP_Protection_LevelEnumeration, _COPP_HDCP_Protection_Level, dshow.copp_hdcp_protection_level, dxva9typ/COPP_HDCP_ForceDWORD, dxva9typ/COPP_HDCP_Level0, dxva9typ/COPP_HDCP_Level1, dxva9typ/COPP_HDCP_LevelMax, dxva9typ/COPP_HDCP_LevelMin, dxva9typ/COPP_HDCP_Protection_Level
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
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
tech.root: 
req.typenames: COPP_HDCP_Protection_Level
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva9typ.h
api_name:
-	COPP_HDCP_Protection_Level
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

