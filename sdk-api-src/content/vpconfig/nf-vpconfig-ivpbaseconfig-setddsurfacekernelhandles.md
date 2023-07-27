---
UID: NF:vpconfig.IVPBaseConfig.SetDDSurfaceKernelHandles
title: IVPBaseConfig::SetDDSurfaceKernelHandles (vpconfig.h)
description: The SetDDSurfaceKernelHandles method specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay surface.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetDDSurfaceKernelHandles method","IVPBaseConfig.SetDDSurfaceKernelHandles","IVPBaseConfig::SetDDSurfaceKernelHandles","IVPBaseConfigSetDDSurfaceKernelHandle","SetDDSurfaceKernelHandles","SetDDSurfaceKernelHandles method [DirectShow]","SetDDSurfaceKernelHandles method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setddsurfacekernelhandles","vpconfig/IVPBaseConfig::SetDDSurfaceKernelHandles"]
old-location: dshow\ivpbaseconfig_setddsurfacekernelhandles.htm
tech.root: dshow
ms.assetid: e180f731-a540-4754-93ff-232ad4502c6f
ms.date: 4/26/2023
ms.keywords: IVPBaseConfig interface [DirectShow],SetDDSurfaceKernelHandles method, IVPBaseConfig.SetDDSurfaceKernelHandles, IVPBaseConfig::SetDDSurfaceKernelHandles, IVPBaseConfigSetDDSurfaceKernelHandle, SetDDSurfaceKernelHandles, SetDDSurfaceKernelHandles method [DirectShow], SetDDSurfaceKernelHandles method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setddsurfacekernelhandles, vpconfig/IVPBaseConfig::SetDDSurfaceKernelHandles
req.header: vpconfig.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPBaseConfig::SetDDSurfaceKernelHandles
 - vpconfig/IVPBaseConfig::SetDDSurfaceKernelHandles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetDDSurfaceKernelHandles
---

# IVPBaseConfig::SetDDSurfaceKernelHandles


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDDSurfaceKernelHandles</code> method specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay surface.

## -parameters

### -param cHandles [in]

Specifies the number of handles in the <i>rgDDKernelHandles</i> array.

### -param rgDDKernelHandles [in]

Address of an array of kernel-mode handles.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method sets the DirectDraw handles for the overlay surface. There may be more than one attached surface, so the array may contain more than one surface handle.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>