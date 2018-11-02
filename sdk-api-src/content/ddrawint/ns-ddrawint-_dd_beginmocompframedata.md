---
UID: NS:ddrawint._DD_BEGINMOCOMPFRAMEDATA
title: "_DD_BEGINMOCOMPFRAMEDATA"
author: windows-sdk-content
description: The DDHAL_BEGINMOCOMPFRAMEDATA structure contains the frame information required to start decoding.
old-location: display\dd_beginmocompframedata.htm
tech.root: display
ms.assetid: 4a75642d-87e3-4c95-be67-2d494bf6122e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PDD_BEGINMOCOMPFRAMEDATA, DD_BEGINMOCOMPFRAMEDATA, DD_BEGINMOCOMPFRAMEDATA structure [Display Devices], _DD_BEGINMOCOMPFRAMEDATA, ddrawint/DD_BEGINMOCOMPFRAMEDATA, ddstrcts_6e61d707-7245-4d0d-aaa5-f63bb610d2e5.xml, display.dd_beginmocompframedata"
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
 - DD_BEGINMOCOMPFRAMEDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_BEGINMOCOMPFRAMEDATA, DD_BEGINMOCOMPFRAMEDATA"
req.redist: 
---

# _DD_BEGINMOCOMPFRAMEDATA structure


## -description


The DDHAL_BEGINMOCOMPFRAMEDATA structure contains the frame information required to start decoding. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/41cde03a-f9da-4701-a0df-0dba0c17ba26">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.


### -field lpDestSurface

Points to a <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure representing the destination surface in which to decode this frame.


### -field dwInputDataSize

Indicates the size in bytes of optional input data in <b>lpInputData</b> that is required to begin this frame. 


### -field lpInputData

Points to an optional input buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers. 


### -field dwOutputDataSize

Indicates the size in bytes of optional output data in <b>lpOutputData</b> that is required to begin this frame.


### -field lpOutputData

Points to an optional output buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/0038aedc-2e4f-4d89-878f-7f6f751015cc">DdMoCompBeginFrame</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/0038aedc-2e4f-4d89-878f-7f6f751015cc">DdMoCompBeginFrame</a>
 

 

