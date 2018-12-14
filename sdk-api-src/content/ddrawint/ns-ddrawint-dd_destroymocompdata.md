---
UID: NS:ddrawint._DD_DESTROYMOCOMPDATA
title: DD_DESTROYMOCOMPDATA
author: windows-sdk-content
description: The DD_DESTROYMOCOMPDATA structure contains the information required to finish performing motion compensation.
old-location: display\dd_destroymocompdata.htm
tech.root: display
ms.assetid: 0db32ded-2e32-471d-a752-1f5beffec684
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDD_DESTROYMOCOMPDATA, DD_DESTROYMOCOMPDATA, DD_DESTROYMOCOMPDATA structure [Display Devices], ddrawint/DD_DESTROYMOCOMPDATA, ddstrcts_1a3d548c-c0f7-4334-b0c6-b63c155d854c.xml, display.dd_destroymocompdata"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DD_DESTROYMOCOMPDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_DESTROYMOCOMPDATA, DD_DESTROYMOCOMPDATA"
req.redist: 
---

# DD_DESTROYMOCOMPDATA structure


## -description


The DD_DESTROYMOCOMPDATA structure contains the information required to finish performing motion compensation. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/41cde03a-f9da-4701-a0df-0dba0c17ba26">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/7a8900d0-4c9f-4600-8408-197f4e7c78ba">DdMoCompDestroy</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/7a8900d0-4c9f-4600-8408-197f4e7c78ba">DdMoCompDestroy</a>
 

 

