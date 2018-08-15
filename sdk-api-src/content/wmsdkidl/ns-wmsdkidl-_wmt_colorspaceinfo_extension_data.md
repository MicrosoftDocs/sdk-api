---
UID: NS:wmsdkidl._WMT_COLORSPACEINFO_EXTENSION_DATA
title: "_WMT_COLORSPACEINFO_EXTENSION_DATA"
author: windows-sdk-content
description: The WMT_COLORSPACEINFO_EXTENSION_DATA structure contains information about the color format of output video samples. It is used as the value for the WM_SampleExtensionGUID_ColorSpaceInfo data unit extension.
old-location: wmformat\wmt_colorspaceinfo_extension_data.htm
old-project: wmformat
ms.assetid: 0d512d6a-95d5-4ca1-aee2-ca19319e1b83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WMT_COLORSPACEINFO_EXTENSION_DATA, WMT_COLORSPACEINFO_EXTENSION_DATA structure [windows Media Format], _WMT_COLORSPACEINFO_EXTENSION_DATA, wmformat.wmt_colorspaceinfo_extension_data, wmsdkidl/WMT_COLORSPACEINFO_EXTENSION_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WMT_COLORSPACEINFO_EXTENSION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_COLORSPACEINFO_EXTENSION_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

