---
UID: NS:ddrawint._DD_QUERYMOCOMPSTATUSDATA
title: "_DD_QUERYMOCOMPSTATUSDATA"
author: windows-sdk-content
description: The DD_QUERYMOCOMPSTATUSDATA structure contains information required to query the status of the previous frame.
old-location: display\dd_querymocompstatusdata.htm
tech.root: display
ms.assetid: 53e2c8c7-dc6b-4c0b-9555-9aac07bd9186
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PDD_QUERYMOCOMPSTATUSDATA, DD_QUERYMOCOMPSTATUSDATA, DD_QUERYMOCOMPSTATUSDATA structure [Display Devices], _DD_QUERYMOCOMPSTATUSDATA, ddrawint/DD_QUERYMOCOMPSTATUSDATA, ddstrcts_d8a10a3c-886c-4cef-b4a0-2db5f4c45927.xml, display.dd_querymocompstatusdata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_QUERYMOCOMPSTATUSDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_QUERYMOCOMPSTATUSDATA, DD_QUERYMOCOMPSTATUSDATA"
req.redist: 
---

# _DD_QUERYMOCOMPSTATUSDATA structure


## -description


The DD_QUERYMOCOMPSTATUSDATA structure contains information required to query the status of the previous frame. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/41cde03a-f9da-4701-a0df-0dba0c17ba26">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.


### -field lpSurface

Points to a <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure that contains the surface being queried. 


### -field dwFlags

Indicates the type of surface access.





#### DDMCQUERY_READ

Indicates that the surface can only be tested for read or display access. If this flag is not set, the surface can be tested for write access.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/af62d169-665a-43d2-ac0c-cc8ce6ce42d0">DdMoCompQueryStatus</a> callback. A return code of DD_OK indicates the hardware has finished processing the <a href="https://msdn.microsoft.com/d88f2c7e-e3e5-4444-836c-a45d52c86e54">DdMoCompRender</a> request. Otherwise the return value must be DDERR_WASSTILLDRAWING. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/af62d169-665a-43d2-ac0c-cc8ce6ce42d0">DdMoCompQueryStatus</a>



<a href="https://msdn.microsoft.com/d88f2c7e-e3e5-4444-836c-a45d52c86e54">DdMoCompRender</a>
 

 

