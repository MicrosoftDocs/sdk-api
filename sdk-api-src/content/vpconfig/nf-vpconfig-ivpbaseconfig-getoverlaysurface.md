---
UID: NF:vpconfig.IVPBaseConfig.GetOverlaySurface
title: IVPBaseConfig::GetOverlaySurface (vpconfig.h)
description: The GetOverlaySurface method queries whether the caller should use the driver's overlay surface. If so, the method returns a pointer to the surface.
helpviewer_keywords: ["GetOverlaySurface","GetOverlaySurface method [DirectShow]","GetOverlaySurface method [DirectShow]","IVPBaseConfig interface","IVPBaseConfig interface [DirectShow]","GetOverlaySurface method","IVPBaseConfig.GetOverlaySurface","IVPBaseConfig::GetOverlaySurface","IVPBaseConfigGetOverlaySurface","dshow.ivpbaseconfig_getoverlaysurface","vpconfig/IVPBaseConfig::GetOverlaySurface"]
old-location: dshow\ivpbaseconfig_getoverlaysurface.htm
tech.root: dshow
ms.assetid: a4d4b63f-b84c-4831-b16e-c0042b54a215
ms.date: 12/05/2018
ms.keywords: GetOverlaySurface, GetOverlaySurface method [DirectShow], GetOverlaySurface method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetOverlaySurface method, IVPBaseConfig.GetOverlaySurface, IVPBaseConfig::GetOverlaySurface, IVPBaseConfigGetOverlaySurface, dshow.ivpbaseconfig_getoverlaysurface, vpconfig/IVPBaseConfig::GetOverlaySurface
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
 - IVPBaseConfig::GetOverlaySurface
 - vpconfig/IVPBaseConfig::GetOverlaySurface
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
 - IVPBaseConfig.GetOverlaySurface
---

# IVPBaseConfig::GetOverlaySurface


## -description

The <code>GetOverlaySurface</code> method queries whether the caller should use the driver's overlay surface. If so, the method returns a pointer to the surface.

## -parameters

### -param ppddOverlaySurface [out]

Address of a pointer to the <b>IDirectDrawSurface</b> interface. If the caller should use the driver's overlay surface, it sets this variable equal to the <b>IDirectDrawSurface</b> interface for the overlay surface.

## -returns

Returns S_OK if the overlay surface object was returned.

## -remarks

The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> uses this function to determine if the driver requires the Overlay Mixer to use the driver's overlay surface. If this function returns <b>NULL</b>, then the Overlay Mixer allocates its own surface.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>