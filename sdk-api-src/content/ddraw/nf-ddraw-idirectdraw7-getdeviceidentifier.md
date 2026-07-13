---
UID: NF:ddraw.IDirectDraw7.GetDeviceIdentifier
title: IDirectDraw7::GetDeviceIdentifier (ddraw.h)
description: Obtains information about the device driver. This method can be used, with caution, to recognize specific hardware installations to implement workarounds for poor driver or chipset behavior.
helpviewer_keywords: ["DDGDI_GETHOSTIDENTIFIER","GetDeviceIdentifier","GetDeviceIdentifier method [DirectDraw]","GetDeviceIdentifier method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetDeviceIdentifier method","IDirectDraw7.GetDeviceIdentifier","IDirectDraw7::GetDeviceIdentifier","ddraw/IDirectDraw7::GetDeviceIdentifier","directdraw.idirectdraw7_getdeviceidentifier"]
old-location: directdraw\idirectdraw7_getdeviceidentifier.htm
tech.root: directdraw
ms.assetid: 1524dae8-e383-47f4-8e18-c8ef235b3176
ms.date: 12/05/2018
ms.keywords: DDGDI_GETHOSTIDENTIFIER, GetDeviceIdentifier, GetDeviceIdentifier method [DirectDraw], GetDeviceIdentifier method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetDeviceIdentifier method, IDirectDraw7.GetDeviceIdentifier, IDirectDraw7::GetDeviceIdentifier, ddraw/IDirectDraw7::GetDeviceIdentifier, directdraw.idirectdraw7_getdeviceidentifier
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
 - IDirectDraw7::GetDeviceIdentifier
 - ddraw/IDirectDraw7::GetDeviceIdentifier
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
 - IDirectDraw7.GetDeviceIdentifier
---

# IDirectDraw7::GetDeviceIdentifier


## -description

Obtains information about the device driver. This method can be used, with caution, to recognize specific hardware installations to implement workarounds for poor driver or chipset behavior.

## -parameters

### -param unnamedParam1 [out]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-dddeviceidentifier2">DDDEVICEIDENTIFIER2</a> structure that receives information about the driver.

### -param unnamedParam2 [in]

This value consists of flags that specify options. The following flag is the only defined flag:



#### DDGDI_GETHOSTIDENTIFIER

Causes <b>GetDeviceIdentifier</b> to return information about the host (typically 2-D) adapter in a system equipped with a stacked secondary 3-D adapter. Such an adapter appears to the application as if it were part of the host adapter, but is typically located on a separate card. When the <i>dwFlags</i> parameter is 0, information on the stacked secondary is returned because this most accurately reflects the qualities of the DirectDraw object involved.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return DDERR_INVALIDPARAMS.

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>