---
UID: NS:wingdi._RASTERIZER_STATUS
title: "_RASTERIZER_STATUS"
author: windows-sdk-content
description: The RASTERIZER_STATUS structure contains information about whether TrueType is installed. This structure is filled when an application calls the GetRasterizerCaps function.
old-location: gdi\rasterizer_status.htm
old-project: gdi
ms.assetid: 40bb4b59-90a4-4780-ae5f-fef8a6fa62cb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPRASTERIZER_STATUS, LPRASTERIZER_STATUS, LPRASTERIZER_STATUS structure pointer [Windows GDI], RASTERIZER_STATUS, RASTERIZER_STATUS structure [Windows GDI], _RASTERIZER_STATUS, _win32_RASTERIZER_STATUS_str, gdi.rasterizer_status, wingdi/LPRASTERIZER_STATUS, wingdi/RASTERIZER_STATUS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: RASTERIZER_STATUS, *LPRASTERIZER_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	RASTERIZER_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _RASTERIZER_STATUS structure


## -description



The <b>RASTERIZER_STATUS</b> structure contains information about whether TrueType is installed. This structure is filled when an application calls the <a href="https://msdn.microsoft.com/0898d1c0-5480-4bd2-aa45-918340172a05">GetRasterizerCaps</a> function.




## -struct-fields




### -field nSize

The size, in bytes, of the <b>RASTERIZER_STATUS</b> structure.


### -field wFlags

Specifies whether at least one TrueType font is installed and whether TrueType is enabled. This value is TT_AVAILABLE, TT_ENABLED, or both if TrueType is on the system.


### -field nLanguageID

The language in the system's Setup.inf file.


## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/0898d1c0-5480-4bd2-aa45-918340172a05">GetRasterizerCaps</a>
 

 

