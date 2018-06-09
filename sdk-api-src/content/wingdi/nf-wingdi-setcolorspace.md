---
UID: NF:wingdi.SetColorSpace
title: SetColorSpace function
author: windows-sdk-content
description: The SetColorSpace function defines the input color space for a given device context.
old-location: wcs\setcolorspace.htm
old-project: WCS
ms.assetid: 037c864f-f8ec-4467-9236-74ea4493d743
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SetColorSpace, SetColorSpace function [Windows Color System], _color_SetColorSpace, wcs.setcolorspace, wingdi/SetColorSpace
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetColorSpace function


## -description


The <b>SetColorSpace</b> function defines the input <a href="https://www.bing.com/search?q=color+space">color space</a> for a given device context.


## -parameters




### -param hdc

TBD


### -param hcs

TBD




#### - hColorSpace

Identifies handle to the color space to set.


#### - hDC

Specifies the handle to a device context.


## -returns



If this function succeeds, the return value is a handle to the <i>hColorSpace</i> being replaced.

If this function fails, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

