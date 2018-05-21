---
UID: NF:wingdi.GetRasterizerCaps
title: GetRasterizerCaps function
author: windows-driver-content
description: The GetRasterizerCaps function returns flags indicating whether TrueType fonts are installed in the system.
old-location: gdi\getrasterizercaps.htm
old-project: gdi
ms.assetid: 0898d1c0-5480-4bd2-aa45-918340172a05
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetRasterizerCaps, GetRasterizerCaps function [Windows GDI], _win32_GetRasterizerCaps, gdi.getrasterizercaps, wingdi/GetRasterizerCaps
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	GetRasterizerCaps
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetRasterizerCaps function


## -description


The <b>GetRasterizerCaps</b> function returns flags indicating whether TrueType fonts are installed in the system.


## -parameters




### -param lpraststat

TBD


### -param cjBytes

TBD




#### - cb [in]

The number of bytes to be copied into the structure pointed to by the <i>lprs</i> parameter.


#### - lprs [out]

A pointer to a <a href="https://msdn.microsoft.com/40bb4b59-90a4-4780-ae5f-fef8a6fa62cb">RASTERIZER_STATUS</a> structure that receives information about the rasterizer.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetRasterizerCaps</b> function enables applications and printer drivers to determine whether TrueType fonts are installed.

If the TT_AVAILABLE flag is set in the <b>wFlags</b> member of the <a href="https://msdn.microsoft.com/40bb4b59-90a4-4780-ae5f-fef8a6fa62cb">RASTERIZER_STATUS</a> structure, at least one TrueType font is installed. If the TT_ENABLED flag is set, TrueType is enabled for the system.

The actual number of bytes copied is either the member specified in the <i>cb</i> parameter or the length of the <a href="https://msdn.microsoft.com/40bb4b59-90a4-4780-ae5f-fef8a6fa62cb">RASTERIZER_STATUS</a> structure, whichever is less.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b8c7a557-ca35-41a4-9043-8496e5b01564">GetOutlineTextMetrics</a>



<a href="https://msdn.microsoft.com/40bb4b59-90a4-4780-ae5f-fef8a6fa62cb">RASTERIZER_STATUS</a>
 

 

