---
UID: NF:ddraw.IDirectDraw7.GetCaps
title: IDirectDraw7::GetCaps (ddraw.h)
description: Retrieves the capabilities of the device driver for the hardware and the hardware emulation layer (HEL).
helpviewer_keywords: ["GetCaps","GetCaps method [DirectDraw]","GetCaps method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetCaps method","IDirectDraw7.GetCaps","IDirectDraw7::GetCaps","ddraw/IDirectDraw7::GetCaps","directdraw.idirectdraw7_getcaps"]
old-location: directdraw\idirectdraw7_getcaps.htm
tech.root: directdraw
ms.assetid: 4e93612c-9e28-4d51-a640-e8e9b5ed8e7a
ms.date: 12/05/2018
ms.keywords: GetCaps, GetCaps method [DirectDraw], GetCaps method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetCaps method, IDirectDraw7.GetCaps, IDirectDraw7::GetCaps, ddraw/IDirectDraw7::GetCaps, directdraw.idirectdraw7_getcaps
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
 - IDirectDraw7::GetCaps
 - ddraw/IDirectDraw7::GetCaps
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
 - IDirectDraw7.GetCaps
---

# IDirectDraw7::GetCaps


## -description

Retrieves the capabilities of the device driver for the hardware and the hardware emulation layer (HEL).

## -parameters

### -param unnamedParam1 [out]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS</a> structure that receives the capabilities of the hardware, as reported by the device driver. Set this parameter to NULL if you do not want to retrieve device driver capabilities.

### -param unnamedParam2 [out]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS</a> structure that receives the capabilities of the HEL. Set this parameter to NULL if you do not want to retrieve HEL capabilities.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>
You can set only one of the two parameters to NULL to exclude it. If you set both to NULL, the method fails and returns DDERR_INVALIDPARAMS.

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>