---
UID: NF:wingdi.SetColorSpace
title: SetColorSpace function
author: windows-sdk-content
description: The SetColorSpace function defines the input color space for a given device context.
old-location: wcs\setcolorspace.htm
tech.root: WCS
ms.assetid: 037c864f-f8ec-4467-9236-74ea4493d743
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetColorSpace, SetColorSpace function [Windows Color System], _color_SetColorSpace, wcs.setcolorspace, wingdi/SetColorSpace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetColorSpace
: 
---

# SetColorSpace function


## -description


The <b>SetColorSpace</b> function defines the input <a href="https://msdn.microsoft.com/en-us/library/Dd371818(v=VS.85).aspx">color space</a> for a given device context.


## -parameters




### -param hdc

Specifies the handle to a device context.


### -param hcs

Identifies handle to the color space to set.


## -returns



If this function succeeds, the return value is a handle to the <i>hColorSpace</i> being replaced.

If this function fails, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

