---
UID: NF:dwrite.IDWriteRenderingParams.GetClearTypeLevel
title: IDWriteRenderingParams::GetClearTypeLevel
author: windows-sdk-content
description: Gets the ClearType level of the rendering parameters object.
old-location: directwrite\IDWriteRenderingParams_GetClearTypeLevel.htm
tech.root: DirectWrite
ms.assetid: 62b2aa39-ca8f-4abd-af10-1c1ca7971dcd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetClearTypeLevel, GetClearTypeLevel method [Direct Write], GetClearTypeLevel method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetClearTypeLevel method, IDWriteRenderingParams.GetClearTypeLevel, IDWriteRenderingParams::GetClearTypeLevel, directwrite.IDWriteRenderingParams_GetClearTypeLevel, dwrite/IDWriteRenderingParams::GetClearTypeLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteRenderingParams.GetClearTypeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteRenderingParams.GetClearTypeLevel
: 
---

# IDWriteRenderingParams::GetClearTypeLevel


## -description


Gets the ClearType level of the rendering parameters object. 


## -parameters






## -returns



Type: <b>FLOAT</b>

The ClearType level of the rendering parameters object.




## -remarks



The ClearType level represents the amount of ClearType – that is, the degree to which the red, green, and blue subpixels of each pixel are treated differently. Valid values range from zero (meaning no ClearType, which is equivalent to grayscale anti-aliasing) to one (meaning full ClearType)




## -see-also




<a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>
 

 

