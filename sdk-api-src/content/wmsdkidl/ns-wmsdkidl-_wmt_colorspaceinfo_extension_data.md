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

# _WMT_COLORSPACEINFO_EXTENSION_DATA structure


## -description



The <b>WMT_COLORSPACEINFO_EXTENSION_DATA</b> structure contains information about the color format of output video samples. It is used as the value for the WM_SampleExtensionGUID_ColorSpaceInfo data unit extension.




## -struct-fields




### -field ucColorPrimaries

Specifies the chromaticity coordinates of the color primaries.


### -field ucColorTransferChar

Specifies the opto-electronic transfer characteristics of the source picture.


### -field ucColorMatrixCoef

Specifies the matrix coefficients used to derive Y, Cb, and Cr signals from the color primaries.


## -see-also




<a href="https://msdn.microsoft.com/8de2e003-cb21-4be9-bcde-7f5909b6260a">Sample Extension Types</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

