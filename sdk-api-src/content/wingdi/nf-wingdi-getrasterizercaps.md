---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

