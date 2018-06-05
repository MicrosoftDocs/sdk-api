---
UID: NF:wingdi.GetAspectRatioFilterEx
title: GetAspectRatioFilterEx function
author: windows-sdk-content
description: The GetAspectRatioFilterEx function retrieves the setting for the current aspect-ratio filter.
old-location: gdi\getaspectratiofilterex.htm
old-project: gdi
ms.assetid: 3f2dd47d-08bf-4848-897f-5ae506fba342
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetAspectRatioFilterEx, GetAspectRatioFilterEx function [Windows GDI], _win32_GetAspectRatioFilterEx, gdi.getaspectratiofilterex, wingdi/GetAspectRatioFilterEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetAspectRatioFilterEx
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetAspectRatioFilterEx function


## -description


The <b>GetAspectRatioFilterEx</b> function retrieves the setting for the current aspect-ratio filter.


## -parameters




### -param hdc [in]

Handle to a device context.


### -param lpsize

TBD




#### - lpAspectRatio [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that receives the current aspect-ratio filter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The aspect ratio is the ratio formed by the width and height of a pixel on a specified device.

The system provides a special filter, the aspect-ratio filter, to select fonts that were designed for a particular device. An application can specify that the system should only retrieve fonts matching the specified aspect ratio by calling the <a href="https://msdn.microsoft.com/74cfe0d3-0d20-4382-8e76-55a6e2323308">SetMapperFlags</a> function.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>



<a href="https://msdn.microsoft.com/74cfe0d3-0d20-4382-8e76-55a6e2323308">SetMapperFlags</a>
 

 

