---
UID: NS:ddrawint._DD_ENDMOCOMPFRAMEDATA
title: "_DD_ENDMOCOMPFRAMEDATA"
author: windows-sdk-content
description: The DD_ENDMOCOMPFRAMEDATA structure contains information required to complete a decoded frame.
old-location: display\dd_endmocompframedata.htm
old-project: display
ms.assetid: 4e604940-1c0f-43be-bac7-9936df0c4044
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: "*PDD_ENDMOCOMPFRAMEDATA, DD_ENDMOCOMPFRAMEDATA, DD_ENDMOCOMPFRAMEDATA structure [Display Devices], _DD_ENDMOCOMPFRAMEDATA, ddrawint/DD_ENDMOCOMPFRAMEDATA, ddstrcts_4c526986-eaf4-40ea-890c-e90295ac9ee6.xml, display.dd_endmocompframedata"
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
tech.root: 
req.typenames: "*PDD_ENDMOCOMPFRAMEDATA, DD_ENDMOCOMPFRAMEDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_ENDMOCOMPFRAMEDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_ENDMOCOMPFRAMEDATA structure


## -description


The DD_ENDMOCOMPFRAMEDATA structure contains information required to complete a decoded frame. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551663">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.


### -field lpInputData

Points to an optional buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers.


### -field dwInputDataSize

Indicates the size in bytes of data in <b>lpInputData</b>. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/3589f003-32fc-44c4-867a-abf54f347de9">DdMoCompEndFrame</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/3589f003-32fc-44c4-867a-abf54f347de9">DdMoCompEndFrame</a>
 

 

