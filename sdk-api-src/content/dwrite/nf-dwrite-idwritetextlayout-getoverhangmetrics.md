---
UID: NF:dwrite.IDWriteTextLayout.GetOverhangMetrics
title: IDWriteTextLayout::GetOverhangMetrics
author: windows-sdk-content
description: Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.
old-location: directwrite\idwritetextlayout_getoverhangmetrics.htm
tech.root: DirectWrite
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOverhangMetrics, GetOverhangMetrics method [Direct Write], GetOverhangMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetOverhangMetrics method, IDWriteTextLayout.GetOverhangMetrics, IDWriteTextLayout::GetOverhangMetrics, directwrite.idwritetextlayout_getoverhangmetrics, dwrite/IDWriteTextLayout::GetOverhangMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteTextLayout.GetOverhangMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetOverhangMetrics


## -description


Returns the overhangs (in DIPs) of the layout and all
    objects contained in it, including text glyphs and inline objects.


## -parameters




### -param overhangs [out]

Type: <b><a href="https://msdn.microsoft.com/a285f06b-a4d0-4ebe-80f5-157e59bfba31">DWRITE_OVERHANG_METRICS</a>*</b>

Overshoots of visible extents (in DIPs) outside the layout.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

