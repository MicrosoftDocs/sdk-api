---
UID: NF:icm.WcsGetDefaultRenderingIntent
title: WcsGetDefaultRenderingIntent function
author: windows-sdk-content
description: Retrieves the default rendering intent in the specified profile management scope.
old-location: wcs\wcsgetdefaultrenderingintent.htm
tech.root: WCS
ms.assetid: 1bb1c09d-1d8a-4568-bdb3-c051781495fa
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WcsGetDefaultRenderingIntent, WcsGetDefaultRenderingIntent function [Windows Color System], _color_WcsGetDefaultRenderingIntent, icm/WcsGetDefaultRenderingIntent, wcs.wcsgetdefaultrenderingintent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mscms.dll
api_name:
 - WcsGetDefaultRenderingIntent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WcsGetDefaultRenderingIntent
: 
---

# WcsGetDefaultRenderingIntent function


## -description


Retrieves the default rendering intent in the specified profile management scope.


## -parameters




### -param scope [in]

The profile management scope for this operation, which can be system-wide or the current user only.


### -param pdwRenderingIntent [out]

A pointer to the variable that will hold the rendering intent.

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function does not revert to the system-wide scope if you do not set the per-user default rendering intent. Instead, it fails, which allows the calling process to distinguish between the per-user and the system-wide setting. If the per-user rendering intent cannot be retrieved, call this function again with system-wide.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

