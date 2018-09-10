---
UID: NF:winddi.PALOBJ_cGetColors
title: PALOBJ_cGetColors function
author: windows-sdk-content
description: The PALOBJ_cGetColors function copies RGB colors from an indexed palette.
old-location: display\palobj_cgetcolors.htm
tech.root: display
ms.assetid: c6bce32f-4daa-41e4-a495-8a3b56d70efc
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: PALOBJ_cGetColors, PALOBJ_cGetColors function [Display Devices], display.palobj_cgetcolors, gdifncs_b7181e52-6f68-4901-9d52-1791a973e6d6.xml, winddi/PALOBJ_cGetColors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - PALOBJ_cGetColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PALOBJ_cGetColors function


## -description


The <b>PALOBJ_cGetColors</b> function copies RGB colors from an indexed palette.


## -parameters




### -param ppalo

Pointer to the <a href="https://msdn.microsoft.com/7c126067-eff8-4387-9fa7-2cde60796471">PALOBJ</a> structure that contains the RGB colors to be copied.


### -param iStart

Specifies the starting color index.


### -param cColors

Specifies the number of colors to be written.


### -param pulColors

Pointer to the buffer in which the colors are to be written.


## -returns



The return value is the number of colors written if the function is successful. Otherwise, it is zero.




## -remarks



A graphics driver can call this function in its implementation of <a href="https://msdn.microsoft.com/b7be48e6-188b-4b23-a494-30adcc18f12e">DrvSetPalette</a>.




## -see-also




<a href="https://msdn.microsoft.com/b7be48e6-188b-4b23-a494-30adcc18f12e">DrvSetPalette</a>



<a href="https://msdn.microsoft.com/7c126067-eff8-4387-9fa7-2cde60796471">PALOBJ</a>
 

 

