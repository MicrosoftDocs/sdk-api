---
UID: NF:icm.TranslateColors
title: TranslateColors function
author: windows-sdk-content
description: The TranslateColors function translates an array of colors from the source color space to the destination color space as defined by a color transform.
old-location: wcs\translatecolors.htm
tech.root: WCS
ms.assetid: 74e9d27d-3cbe-4766-b568-b961de57a610
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TranslateColors, TranslateColors function [Windows Color System], _color_TranslateColors, icm/TranslateColors, wcs.translatecolors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Mscms.dll
api_name:
 - TranslateColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TranslateColors
: 
---

# TranslateColors function


## -description


The <b>TranslateColors</b> function translates an array of colors from the source <a href="c.htm">color space</a> to the destination color space as defined by a color transform.


## -parameters




### -param hColorTransform

Identifies the color transform to use.


### -param paInputColors

Pointer to an array of <i>nColors</i><a href="color.htm">COLOR</a> structures to translate.


### -param nColors

Contains the number of elements in the arrays pointed to by <i>paInputColors</i> and <i>paOutputColors</i>.


### -param ctInput

Specifies the input color type.


### -param paOutputColors

Pointer to an array of <i>nColors</i><b>COLOR</b> structures that receive the translated colors.


### -param ctOutput

Specifies the output color type.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the input and the output color types are not compatible with the color transform, this function fails.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

