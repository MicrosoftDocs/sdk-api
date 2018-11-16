---
UID: NF:icm.WcsCheckColors
title: WcsCheckColors function
author: windows-sdk-content
description: Determines whether the colors in an array are within the output gamut of a specified WCS color transform.
old-location: wcs\wcscheckcolors.htm
tech.root: WCS
ms.assetid: 01b452bf-4352-4b83-863b-e9eb76121fdd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WcsCheckColors, WcsCheckColors function [Windows Color System], _color_WcsCheckColors, icm/WcsCheckColors, wcs.wcscheckcolors
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
 - WcsCheckColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WcsCheckColors
: 
---

# WcsCheckColors function


## -description


Determines whether the colors in an array are within the output gamut of a specified WCS color transform.


## -parameters




### -param hColorTransform [in]

A handle to the specified WCS color transform.


### -param nColors [in]

The number of elements in the array pointed to by <i>pInputData</i> and <i>paResult</i>.


### -param nInputChannels [in]

The number of channels per element in the array pointed to by <i>pInputData</i>.


### -param cdtInput [in]

The input COLORDATATYPE color data type.


### -param cbInput [in]

The buffer size of <i>pInputData</i>.


### -param pInputData [in]

A pointer to an array of input colors. Colors in this array correspond to the color space of the source profile. The size of the buffer for this array will be the number of bytes indicated by <i>cbInput</i>.


### -param paResult [out]

A pointer to an array of <i>nColors</i> bytes that receives the results of the test. 


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the input and the output color data types are not compatible with the color transform, this function will convert the input color data as required.

This function fails if you use an International Color Consortium (ICC) transform is used.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

