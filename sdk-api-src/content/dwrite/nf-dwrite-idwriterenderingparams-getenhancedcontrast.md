---
UID: NF:dwrite.IDWriteRenderingParams.GetEnhancedContrast
title: IDWriteRenderingParams::GetEnhancedContrast
author: windows-sdk-content
description: Gets the enhanced contrast property of the rendering parameters object. Valid values are greater than or equal to zero.
old-location: directwrite\IDWriteRenderingParams_GetEnhancedContrast.htm
tech.root: DirectWrite
ms.assetid: dabce803-4989-4532-bf96-2f7eb09b29fe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnhancedContrast, GetEnhancedContrast method [Direct Write], GetEnhancedContrast method [Direct Write],IDWriteRenderingParams interface, IDWriteRenderingParams interface [Direct Write],GetEnhancedContrast method, IDWriteRenderingParams.GetEnhancedContrast, IDWriteRenderingParams::GetEnhancedContrast, directwrite.IDWriteRenderingParams_GetEnhancedContrast, dwrite/IDWriteRenderingParams::GetEnhancedContrast
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
 - IDWriteRenderingParams.GetEnhancedContrast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRenderingParams::GetEnhancedContrast


## -description


Gets the enhanced contrast property of the rendering parameters object. Valid values are greater than or equal to zero.


## -parameters






## -returns



Type: <b>FLOAT</b>

Returns the amount of contrast enhancement. Valid values are greater than
     or equal to zero.




## -remarks



Enhanced contrast is the amount to increase the darkness of text, and typically ranges from 0 to 1. Zero means no contrast enhancement.




## -see-also




<a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>
 

 

