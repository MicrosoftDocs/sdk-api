---
UID: NF:icm.WcsTranslateColors
title: WcsTranslateColors function
author: windows-sdk-content
description: Translates an array of colors from the source color space to the destination color space as defined by a color transform.
old-location: wcs\wcstranslatecolors.htm
tech.root: WCS
ms.assetid: e7053c70-5b32-4d33-983c-a4c9c14a0d1b
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WcsTranslateColors, WcsTranslateColors function [Windows Color System], _color_WcsTranslateColors, icm/WcsTranslateColors, wcs.wcstranslatecolors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - WcsTranslateColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsTranslateColors function


## -description


Translates an array of colors from the source color space to the destination color space as defined by a color transform.


## -parameters




### -param hColorTransform [in]

A handle for the WCS color transform.


### -param nColors [in]

The number of elements in the array to which <i>pInputData</i> and <i>pOutputData</i> point.


### -param nInputChannels [in]

The number of channels per element in the array to which <i>pInputData</i> points.


### -param cdtInput [in]

The input <a href="https://msdn.microsoft.com/001001c2-9a34-4d70-937d-befa0fc2118c">COLORDATATYPE</a> color data type.


### -param cbInput [in]

The buffer size, in bytes, of <i>pInputData</i>.


### -param pInputData [in]

A pointer to an array of input colors. The size of the buffer for this array, in bytes, is the <b>DWORD</b> value of <i>cbInput</i>.  


### -param nOutputChannels [in]

The number of channels per element in the array to which <i>pOutputData</i> points.


### -param cdtOutput [in]

The <a href="https://msdn.microsoft.com/001001c2-9a34-4d70-937d-befa0fc2118c">COLORDATATYPE</a> output that specified the color data type.


### -param cbOutput [in]

The buffer size, in bytes, of <i>pOutputData</i>.


### -param pOutputData [out]

A pointer to an array of colors that receives the results of the color translation.The size of the buffer for this array, in bytes, is the <b>DWORD</b> value of <i>cbOutput</i>.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the input and the output color data types are not compatible with the color transform, this function fails. This function will fail if an ICC transform is used.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

