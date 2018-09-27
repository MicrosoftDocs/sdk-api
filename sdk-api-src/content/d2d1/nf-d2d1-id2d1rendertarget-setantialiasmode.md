---
UID: NF:d2d1.ID2D1RenderTarget.SetAntialiasMode
title: ID2D1RenderTarget::SetAntialiasMode
author: windows-sdk-content
description: Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.
old-location: direct2d\ID2D1RenderTarget_SetAntialiasMode.htm
tech.root: direct2d
ms.assetid: cd727271-1725-48e1-be39-680b363db2ae
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SetAntialiasMode method, ID2D1RenderTarget.SetAntialiasMode, ID2D1RenderTarget::SetAntialiasMode, SetAntialiasMode, SetAntialiasMode method [Direct2D], SetAntialiasMode method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SetAntialiasMode, direct2d.ID2D1RenderTarget_SetAntialiasMode
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
 - ID2D1RenderTarget.SetAntialiasMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::SetAntialiasMode


## -description


Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.


## -parameters




### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for future drawing operations. 


## -returns



This method does not return a value.




## -remarks



To specify the antialiasing mode for text and glyph operations, use the <a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a> method. 




## -see-also




<a href="https://msdn.microsoft.com/e9aa93fa-0978-415e-b9f7-802494e81095">GetAntialiasMode</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a>
 

 

