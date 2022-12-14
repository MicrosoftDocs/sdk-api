---
UID: NF:ddraw.IDirectDrawPalette.GetEntries
title: IDirectDrawPalette::GetEntries (ddraw.h)
description: Retrieves palette values from a DirectDrawPalette object.
helpviewer_keywords: ["GetEntries","GetEntries method [DirectDraw]","GetEntries method [DirectDraw]","IDirectDrawPalette interface","IDirectDrawPalette interface [DirectDraw]","GetEntries method","IDirectDrawPalette.GetEntries","IDirectDrawPalette::GetEntries","ddraw/IDirectDrawPalette::GetEntries","directdraw.idirectdrawpalette_getentries"]
old-location: directdraw\idirectdrawpalette_getentries.htm
tech.root: directdraw
ms.assetid: ae3c639f-beb4-40b6-a237-60d6e560a1c3
ms.date: 12/05/2018
ms.keywords: GetEntries, GetEntries method [DirectDraw], GetEntries method [DirectDraw],IDirectDrawPalette interface, IDirectDrawPalette interface [DirectDraw],GetEntries method, IDirectDrawPalette.GetEntries, IDirectDrawPalette::GetEntries, ddraw/IDirectDrawPalette::GetEntries, directdraw.idirectdrawpalette_getentries
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawPalette::GetEntries
 - ddraw/IDirectDrawPalette::GetEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawPalette.GetEntries
---

# IDirectDrawPalette::GetEntries


## -description

Retrieves palette values from a DirectDrawPalette object.

## -parameters

### -param unnamedParam1 [in]

Currently not used and must be set to 0.

### -param unnamedParam2 [in]

Start of the entries to be retrieved sequentially.

### -param unnamedParam3 [in]

Number of palette entries that can fit in the array that <i>lpEntries</i> specifies. The colors of the palette entries are returned in sequence, from the value of the <i>dwStartingEntry</i> parameter through the value of the <i>dwCount</i> parameter minus 1. (These parameters are set by <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-setentries">IDirectDrawPalette::SetEntries</a>.)

### -param unnamedParam4 [out]

An array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures that receives the palette entries from the DirectDrawPalette object. The palette entries are 1 byte each if the DDPCAPS_8BITENTRIES flag is set, and 4 bytes otherwise. Each field is a color description.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTPALETTIZED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a>