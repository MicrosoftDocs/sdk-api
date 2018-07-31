---
UID: NS:winddi._CIECHROMA
title: "_CIECHROMA"
author: windows-sdk-content
description: The CIECHROMA structure is used to describe the chromaticity coordinates, x and y, and the luminance, Y in CIE color space.
old-location: display\ciechroma.htm
old-project: display
ms.assetid: b8d1fd9b-c735-49f6-8d3b-12b5b1d92543
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CIECHROMA, CIECHROMA structure [Display Devices], _CIECHROMA, display.ciechroma, grstrcts_b0ffd3e4-c5c0-40f8-9272-1decae47108d.xml, winddi/CIECHROMA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
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
req.typenames: CIECHROMA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - CIECHROMA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CIECHROMA structure


## -description


The CIECHROMA structure is used to describe the chromaticity coordinates, <b>x</b> and <b>y</b>, and the luminance, <b>Y</b> in CIE color space. 


## -struct-fields




### -field x

Specifies the x-coordinate in CIE chromaticity space.


### -field y

Specifies the y-coordinate in CIE chromaticity space.


### -field Y

Specifies the luminance. For more information, see the following Remarks section.


## -remarks



The CIECHROMA structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539441">COLORINFO</a> structure to define colors for <a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a>.

The LDECI4 type is used to represent real numbers to four decimal places. For example, (LDECI4) 10000 represents the real number 1.0000, and (LDECI4) -12345 represents -1.2345.

The values of the <b>x</b> and <b>y</b> members of CIECHROMA should be in the range from 0 through 10000--that is, the values should represent the numbers 0.0000 through 1.0000. 

The value of the <b>Y</b> member of this structure should be in the range from 0 through 100. This member can also be 65534 (0xFFFE) under certain circumstances. For more information about these circumstances, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff539441">COLORINFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539441">COLORINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a>
 

 

