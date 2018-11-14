---
UID: NF:dwrite.IDWriteTextLayout.GetDrawingEffect
title: IDWriteTextLayout::GetDrawingEffect
author: windows-sdk-content
description: Gets the application-defined drawing effect at the specified text position.
old-location: directwrite\IDWriteTextLayout_GetDrawingEffect.htm
tech.root: DirectWrite
ms.assetid: 1b8d30d1-4da0-40bc-9fee-d06eccae6539
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetDrawingEffect, GetDrawingEffect method [Direct Write], GetDrawingEffect method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetDrawingEffect method, IDWriteTextLayout.GetDrawingEffect, IDWriteTextLayout::GetDrawingEffect, directwrite.IDWriteTextLayout_GetDrawingEffect, dwrite/IDWriteTextLayout::GetDrawingEffect
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
 - IDWriteTextLayout.GetDrawingEffect
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
- IDWriteTextLayout.GetDrawingEffect
: 
---

# IDWriteTextLayout::GetDrawingEffect


## -description


 Gets the application-defined drawing effect at the specified text position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text whose drawing effect is to be retrieved.


### -param drawingEffect [out]

Type: <b>IUnknown**</b>

When this method returns, contains an address of a pointer to  the current application-defined drawing effect. Usually this effect is a foreground brush that  is used in glyph drawing.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

Contains the range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the drawing effect.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

