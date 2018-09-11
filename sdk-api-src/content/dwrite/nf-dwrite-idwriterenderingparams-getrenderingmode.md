---
UID: NF:dwrite.IDWriteRenderingParams.GetRenderingMode
title: IDWriteRenderingParams::GetRenderingMode
author: windows-sdk-content
description: Gets the rendering mode of the rendering parameters object.
old-location: directwrite\IDWriteRenderingParams_GetRenderingMode.htm
tech.root: DirectWrite
ms.assetid: 657360c6-3351-400b-bb41-bcd92de3c48d
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetRenderingMode, GetRenderingMode method [Direct Write], GetRenderingMode method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetRenderingMode method, IDWriteRenderingParams.GetRenderingMode, IDWriteRenderingParams::GetRenderingMode, directwrite.IDWriteRenderingParams_GetRenderingMode, dwrite/IDWriteRenderingParams::GetRenderingMode
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
 - IDWriteRenderingParams.GetRenderingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRenderingParams::GetRenderingMode


## -description


Gets the rendering mode of the rendering parameters object.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a></b>

A value that indicates the rendering mode of the rendering parameters object.




## -remarks



By default, the rendering mode is initialized to DWRITE_RENDERING_MODE_DEFAULT, which means the rendering mode is determined automatically based on the font and size. To determine the recommended rendering mode to use for a given font and size and rendering parameters object, use the <a href="https://msdn.microsoft.com/54504bcb-b05c-4b63-8704-8d718cf2ee16">IDWriteFontFace::GetRecommendedRenderingMode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>
 

 

