---
UID: NF:ddraw.IDirectDraw7.GetMonitorFrequency
title: IDirectDraw7::GetMonitorFrequency (ddraw.h)
description: Retrieves the frequency of the monitor that the DirectDraw object controls.
helpviewer_keywords: ["GetMonitorFrequency","GetMonitorFrequency method [DirectDraw]","GetMonitorFrequency method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetMonitorFrequency method","IDirectDraw7.GetMonitorFrequency","IDirectDraw7::GetMonitorFrequency","ddraw/IDirectDraw7::GetMonitorFrequency","directdraw.idirectdraw7_getmonitorfrequency"]
old-location: directdraw\idirectdraw7_getmonitorfrequency.htm
tech.root: directdraw
ms.assetid: 13f8e5c2-b957-43ce-9fc8-5554c2321bdd
ms.date: 12/05/2018
ms.keywords: GetMonitorFrequency, GetMonitorFrequency method [DirectDraw], GetMonitorFrequency method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetMonitorFrequency method, IDirectDraw7.GetMonitorFrequency, IDirectDraw7::GetMonitorFrequency, ddraw/IDirectDraw7::GetMonitorFrequency, directdraw.idirectdraw7_getmonitorfrequency
f1_keywords:
- ddraw/IDirectDraw7.GetMonitorFrequency
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDraw7.GetMonitorFrequency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the frequency of the monitor that the DirectDraw object controls.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the monitor frequency, in Hertz (Hz).

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>