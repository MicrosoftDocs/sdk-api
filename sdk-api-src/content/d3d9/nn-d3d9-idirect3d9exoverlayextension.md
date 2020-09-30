---
UID: NN:d3d9.IDirect3D9ExOverlayExtension
title: IDirect3D9ExOverlayExtension (d3d9.h)
description: Queries the overlay hardware capabilities of a Direct3D device.
helpviewer_keywords: ["IDirect3D9ExOverlayExtension","IDirect3D9ExOverlayExtension interface [Media Foundation]","IDirect3D9ExOverlayExtension interface [Media Foundation]","described","d3d9/IDirect3D9ExOverlayExtension","mf.idirect3d9exoverlayextension"]
old-location: mf\idirect3d9exoverlayextension.htm
tech.root: mf
ms.assetid: 57591794-96d3-40e6-a4fb-3bb195fd1396
ms.date: 12/05/2018
ms.keywords: IDirect3D9ExOverlayExtension, IDirect3D9ExOverlayExtension interface [Media Foundation], IDirect3D9ExOverlayExtension interface [Media Foundation],described, d3d9/IDirect3D9ExOverlayExtension, mf.idirect3d9exoverlayextension
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IDirect3D9ExOverlayExtension
 - d3d9/IDirect3D9ExOverlayExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3D9ExOverlayExtension
---

# IDirect3D9ExOverlayExtension interface


## -description

Queries the overlay hardware capabilities of a Direct3D device.

To get a pointer to this interface, call <b>QueryInterface</b> on an <b>IDirect3D9Ex</b> interface pointer.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3D9ExOverlayExtension</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3D9ExOverlayExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3D9ExOverlayExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype">CheckDeviceOverlayType</a>
</td>
<td align="left" width="63%">
Queries the overlay hardware capabilities of a Direct3D device.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/direct3d-video-interfaces">Direct3D Video Interfaces</a>



<a href="/windows/desktop/medfound/hardware-overlay-support">Hardware Overlay Support</a>