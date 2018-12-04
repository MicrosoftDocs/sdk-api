---
UID: NF:d2d1.ID2D1RenderTarget.GetTextRenderingParams
title: ID2D1RenderTarget::GetTextRenderingParams
author: windows-sdk-content
description: Retrieves the render target's current text rendering options.
old-location: direct2d\ID2D1RenderTarget_GetTextRenderingParams.htm
tech.root: direct2d
ms.assetid: 563a13c9-7f13-4b38-afa1-72e847dc8349
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetTextRenderingParams, GetTextRenderingParams method [Direct2D], GetTextRenderingParams method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetTextRenderingParams method, ID2D1RenderTarget.GetTextRenderingParams, ID2D1RenderTarget::GetTextRenderingParams, d2d1/ID2D1RenderTarget::GetTextRenderingParams, direct2d.ID2D1RenderTarget_GetTextRenderingParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.GetTextRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::GetTextRenderingParams


## -description


Retrieves the render target's current text rendering options.


## -parameters




### -param textRenderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>**</b>

 When this method returns, <i>textRenderingParams</i>contains the address  of a pointer to the render target's current text rendering options. 


## -returns



This method does not return a value.




## -remarks



If the settings specified by  <i>textRenderingParams</i> are incompatible with the render target's text antialiasing mode (specified by <a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a>), subsequent text and glyph drawing operations will fail and put the render target into an error state.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a>



<a href="https://msdn.microsoft.com/ab4b29a5-72a7-49dc-9131-696f888b0355">SetTextRenderingParams</a>
 

 

