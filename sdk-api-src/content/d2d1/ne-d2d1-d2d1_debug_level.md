---
UID: NE:d2d1.D2D1_DEBUG_LEVEL
title: D2D1_DEBUG_LEVEL
author: windows-sdk-content
description: Indicates the type of information provided by the Direct2D Debug Layer.
old-location: direct2d\D2D1_DEBUG_LEVEL.htm
tech.root: Direct2D
ms.assetid: 3f1b4127-12d4-4472-ae26-0b69fdbb35a7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: D2D1_DEBUG_LEVEL, D2D1_DEBUG_LEVEL enumeration [Direct2D], D2D1_DEBUG_LEVEL_ERROR, D2D1_DEBUG_LEVEL_INFORMATION, D2D1_DEBUG_LEVEL_NONE, D2D1_DEBUG_LEVEL_WARNING, d2d1/D2D1_DEBUG_LEVEL, d2d1/D2D1_DEBUG_LEVEL_ERROR, d2d1/D2D1_DEBUG_LEVEL_INFORMATION, d2d1/D2D1_DEBUG_LEVEL_NONE, d2d1/D2D1_DEBUG_LEVEL_WARNING, direct2d.D2D1_DEBUG_LEVEL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_DEBUG_LEVEL
product: Windows
targetos: Windows
req.typenames: D2D1_DEBUG_LEVEL
req.redist: 
---

# D2D1_DEBUG_LEVEL enumeration


## -description


Indicates the type of information provided by the <a href="https://msdn.microsoft.com/7c28e00b-ebb9-4b79-939c-64eade1351ad">Direct2D Debug Layer</a>.  


## -enum-fields




### -field D2D1_DEBUG_LEVEL_NONE

Direct2D does not produce any debugging output. 


### -field D2D1_DEBUG_LEVEL_ERROR

Direct2D sends error messages to the debug layer.


### -field D2D1_DEBUG_LEVEL_WARNING

Direct2D sends error messages and warnings to the debug layer.


### -field D2D1_DEBUG_LEVEL_INFORMATION

Direct2D sends error messages, warnings, and additional diagnostic information that can help improve performance to the debug layer.  


### -field D2D1_DEBUG_LEVEL_FORCE_DWORD




## -remarks



To receive debugging messages, you must install the <a href="https://msdn.microsoft.com/7c28e00b-ebb9-4b79-939c-64eade1351ad">Direct2D Debug Layer</a>.




## -see-also




<a href="https://msdn.microsoft.com/2765d34e-978c-4121-82c9-2780d54e2850">D2D1_FACTORY_OPTIONS</a>



<a href="https://msdn.microsoft.com/7c28e00b-ebb9-4b79-939c-64eade1351ad">Direct2D Debug Layer</a>
 

 

