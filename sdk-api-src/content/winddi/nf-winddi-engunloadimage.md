---
UID: NF:winddi.EngUnloadImage
title: EngUnloadImage macro (winddi.h)
author: windows-sdk-content
description: The EngUnloadImage function unloads an image loaded by EngLoadImage.
old-location: display\engunloadimage.htm
tech.root: display
ms.assetid: e5b96929-1f57-4b98-8398-69a933e6ff99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngUnloadImage, EngUnloadImage function [Display Devices], display.engunloadimage, gdifncs_e20ef926-cd02-4fdc-bd92-3a9d201b7566.xml, winddi/EngUnloadImage
ms.topic: macro
f1_keywords: 
 - "winddi/EngUnloadImage"
dev_langs:
 - c++
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
 - EngUnloadImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngUnloadImage macro


## -description


The <b>EngUnloadImage</b> function unloads an image loaded by <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>.


## -parameters




### -param h [in]

Handle to the image to be unloaded from system memory.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>
 

 

