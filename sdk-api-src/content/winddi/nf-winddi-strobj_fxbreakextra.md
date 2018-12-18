---
UID: NF:winddi.STROBJ_fxBreakExtra
title: STROBJ_fxBreakExtra function
author: windows-sdk-content
description: The STROBJ_fxBreakExtra function retrieves the amount of extra space to be added to each space character in a string when displaying and/or printing justified text.
old-location: display\strobj_fxbreakextra.htm
tech.root: display
ms.assetid: 857068ab-2c47-402b-a64a-691bdc52a298
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: STROBJ_fxBreakExtra, STROBJ_fxBreakExtra function [Display Devices], display.strobj_fxbreakextra, gdifncs_cfaecb83-e351-447e-ba9d-63ef6dc3f4d8.xml, winddi/STROBJ_fxBreakExtra
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
 - STROBJ_fxBreakExtra
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# STROBJ_fxBreakExtra function


## -description


The <b>STROBJ_fxBreakExtra</b> function retrieves the amount of extra space to be added to each space character in a string when displaying and/or printing justified text.


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a> structure of the string to be displayed.


## -returns



<b>STROBJ_fxBreakExtra</b> returns the amount of extra space to add to each space character in the string. A return value of zero indicates that no extra space is added to space characters in a string.




## -remarks



The extra space value is specified in pixel coordinates.




## -see-also




<a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a>



<a href="https://msdn.microsoft.com/92989c16-5e82-4df2-9298-28b78757bd54">STROBJ_fxCharacterExtra</a>
 

 

