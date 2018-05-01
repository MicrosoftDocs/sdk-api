---
UID: NS:ddrawint._DD_RENDERMOCOMPDATA
title: "_DD_RENDERMOCOMPDATA"
author: windows-driver-content
description: The DD_RENDERMOCOMPDATA structure contains the information required to render a frame.
old-location: display\dd_rendermocompdata.htm
old-project: display
ms.assetid: a890707f-b773-4b66-8817-68efdb8d47f8
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PDD_RENDERMOCOMPDATA, DD_RENDERMOCOMPDATA, DD_RENDERMOCOMPDATA structure [Display Devices], _DD_RENDERMOCOMPDATA, ddrawint/DD_RENDERMOCOMPDATA, ddstrcts_ac8e2378-be85-4257-a664-d757ec914561.xml, display.dd_rendermocompdata"
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
req.typenames: "*PDD_RENDERMOCOMPDATA, DD_RENDERMOCOMPDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_RENDERMOCOMPDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_RENDERMOCOMPDATA structure


## -description


The DD_RENDERMOCOMPDATA structure contains the information required to render a frame. 


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpMoComp

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551663">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.


### -field dwNumBuffers

Indicates the number of entries in the <b>lpBufferInfo</b> member.


### -field lpBufferInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549652">DDMOCOMPBUFFERINFO</a> structure that contains the surfaces and the locations within the surfaces from which to get the macroblock data to render.


### -field dwFunction

Indicates a specific operation the decoder would like the driver to perform. The possible values for this member are defined by the GUID used during motion compensation. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff550529">DD_CREATEMOCOMPDATA</a> for more information.


### -field lpInputData

Points to an optional input buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers.


### -field dwInputDataSize

Specifies the size in bytes of the data pointed to by <b>lpInputData</b>.


### -field lpOutputData

Points to an optional output buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers.


### -field dwOutputDataSize

Specifies the size in bytes of the data pointed to by <b>lpOutputData</b>.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/d88f2c7e-e3e5-4444-836c-a45d52c86e54">DdMoCompRender</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550529">DD_CREATEMOCOMPDATA</a>



<a href="https://msdn.microsoft.com/d88f2c7e-e3e5-4444-836c-a45d52c86e54">DdMoCompRender</a>
 

 

