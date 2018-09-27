---
UID: NF:dwrite.IDWriteTextLayout.SetDrawingEffect
title: IDWriteTextLayout::SetDrawingEffect
author: windows-sdk-content
description: Sets the application-defined drawing effect.
old-location: directwrite\IDWriteTextLayout_SetDrawingEffect.htm
tech.root: DirectWrite
ms.assetid: d3269f8e-c1bc-4e84-92cb-a8899a0268ff
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetDrawingEffect method, IDWriteTextLayout.SetDrawingEffect, IDWriteTextLayout::SetDrawingEffect, SetDrawingEffect, SetDrawingEffect method [Direct Write], SetDrawingEffect method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetDrawingEffect, dwrite/IDWriteTextLayout::SetDrawingEffect
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
 - IDWriteTextLayout.SetDrawingEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::SetDrawingEffect


## -description


 Sets the application-defined drawing effect.


## -parameters




### -param drawingEffect

Type: <b>IUnknown*</b>

Application-defined drawing effects that apply to the range. This data object will be passed back to the application's drawing callbacks for final rendering.


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

The text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An <a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>, such as a color or gradient brush, can be set as a drawing effect if you are using the <a href="https://msdn.microsoft.com/9356071a-35ca-462a-8a77-887e63850586">ID2D1RenderTarget::DrawTextLayout</a> to draw text and that brush will be used to draw the specified range of text.

 This drawing effect is associated with the specified range and will be passed back
     to the application by way of the callback when the range is drawn at drawing time.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

