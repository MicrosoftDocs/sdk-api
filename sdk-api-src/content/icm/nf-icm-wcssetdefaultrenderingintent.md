---
UID: NF:icm.WcsSetDefaultRenderingIntent
title: WcsSetDefaultRenderingIntent function
author: windows-sdk-content
description: Sets the default rendering intent in the specified profile management scope.
old-location: wcs\wcssetdefaultrenderingintent.htm
tech.root: WCS
ms.assetid: 8f0c216c-f501-4b33-92f3-8b2f953a1d2d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WcsSetDefaultRenderingIntent, WcsSetDefaultRenderingIntent function [Windows Color System], _color_WcsSetDefaultRenderingIntent, icm/WcsSetDefaultRenderingIntent, wcs.wcssetdefaultrenderingintent
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
 - WcsSetDefaultRenderingIntent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsSetDefaultRenderingIntent function


## -description


Sets the default rendering intent in the specified profile management scope.


## -parameters




### -param scope [in]

The profile management scope for this operation, which can be system-wide or the current user only.


### -param dwRenderingIntent [in]

The rendering intent. It can be set to one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_SATURATION<div> </div>INTENT_ABSOLUTE_COLORIMETRIC<div> </div>DWORD_MAX

If <i>dwRenderingIntent</i> is DWORD_MAX and <i>scope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, the default rendering intent for the current user reverts to the system-wide default.

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

