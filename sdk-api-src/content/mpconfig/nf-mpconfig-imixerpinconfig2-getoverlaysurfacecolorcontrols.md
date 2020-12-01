---
UID: NF:mpconfig.IMixerPinConfig2.GetOverlaySurfaceColorControls
title: IMixerPinConfig2::GetOverlaySurfaceColorControls (mpconfig.h)
description: The GetOverlaySurfaceColorControls method retrieves the color control settings associated with the specified overlay surface.
helpviewer_keywords: ["GetOverlaySurfaceColorControls","GetOverlaySurfaceColorControls method [DirectShow]","GetOverlaySurfaceColorControls method [DirectShow]","IMixerPinConfig2 interface","IMixerPinConfig2 interface [DirectShow]","GetOverlaySurfaceColorControls method","IMixerPinConfig2.GetOverlaySurfaceColorControls","IMixerPinConfig2::GetOverlaySurfaceColorControls","IMixerPinConfig2GetOverlaySurfaceColorControls","dshow.imixerpinconfig2_getoverlaysurfacecolorcontrols","mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls"]
old-location: dshow\imixerpinconfig2_getoverlaysurfacecolorcontrols.htm
tech.root: dshow
ms.assetid: c6b47e4d-5bf2-4d76-a1e2-88a3342d75a6
ms.date: 12/05/2018
ms.keywords: GetOverlaySurfaceColorControls, GetOverlaySurfaceColorControls method [DirectShow], GetOverlaySurfaceColorControls method [DirectShow],IMixerPinConfig2 interface, IMixerPinConfig2 interface [DirectShow],GetOverlaySurfaceColorControls method, IMixerPinConfig2.GetOverlaySurfaceColorControls, IMixerPinConfig2::GetOverlaySurfaceColorControls, IMixerPinConfig2GetOverlaySurfaceColorControls, dshow.imixerpinconfig2_getoverlaysurfacecolorcontrols, mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls
req.header: mpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMixerPinConfig2::GetOverlaySurfaceColorControls
 - mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig2.GetOverlaySurfaceColorControls
---

# IMixerPinConfig2::GetOverlaySurfaceColorControls


## -description

The <code>GetOverlaySurfaceColorControls</code> method retrieves the color control settings associated with the specified overlay surface.

## -parameters

### -param pColorControl [out]

Address of a pointer to the <b>DDCOLORCONTROL</b> structure containing the color values currently applied to the specified surface.

## -returns

Returns an <b>HRESULT</b> value. If the allocator on the pin is not using an overlay surface, the method returns E_FAIL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig2">IMixerPinConfig2 Interface</a>