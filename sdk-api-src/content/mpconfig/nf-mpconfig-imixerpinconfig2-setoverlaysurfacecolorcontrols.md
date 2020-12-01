---
UID: NF:mpconfig.IMixerPinConfig2.SetOverlaySurfaceColorControls
title: IMixerPinConfig2::SetOverlaySurfaceColorControls (mpconfig.h)
description: Sets the color control settings associated with the specified overlay surface.
helpviewer_keywords: ["IMixerPinConfig2 interface [DirectShow]","SetOverlaySurfaceColorControls method","IMixerPinConfig2.SetOverlaySurfaceColorControls","IMixerPinConfig2::SetOverlaySurfaceColorControls","IMixerPinConfig2SetOverlaySurfaceColorControls","SetOverlaySurfaceColorControls","SetOverlaySurfaceColorControls method [DirectShow]","SetOverlaySurfaceColorControls method [DirectShow]","IMixerPinConfig2 interface","dshow.imixerpinconfig2_setoverlaysurfacecolorcontrols","mpconfig/IMixerPinConfig2::SetOverlaySurfaceColorControls"]
old-location: dshow\imixerpinconfig2_setoverlaysurfacecolorcontrols.htm
tech.root: dshow
ms.assetid: c23c12c9-5621-4b1e-997a-51303f239175
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig2 interface [DirectShow],SetOverlaySurfaceColorControls method, IMixerPinConfig2.SetOverlaySurfaceColorControls, IMixerPinConfig2::SetOverlaySurfaceColorControls, IMixerPinConfig2SetOverlaySurfaceColorControls, SetOverlaySurfaceColorControls, SetOverlaySurfaceColorControls method [DirectShow], SetOverlaySurfaceColorControls method [DirectShow],IMixerPinConfig2 interface, dshow.imixerpinconfig2_setoverlaysurfacecolorcontrols, mpconfig/IMixerPinConfig2::SetOverlaySurfaceColorControls
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
 - IMixerPinConfig2::SetOverlaySurfaceColorControls
 - mpconfig/IMixerPinConfig2::SetOverlaySurfaceColorControls
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
 - IMixerPinConfig2.SetOverlaySurfaceColorControls
---

# IMixerPinConfig2::SetOverlaySurfaceColorControls


## -description

Sets the color control settings associated with the specified overlay surface.

## -parameters

### -param pColorControl [in]

Address of a pointer to the <b>DDCOLORCONTROL</b> structure containing the new values to be applied to the specified surface.

## -returns

Returns an <b>HRESULT</b> value. If the allocator on the pin is not using an overlay surface, the method returns E_FAIL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig2">IMixerPinConfig2 Interface</a>