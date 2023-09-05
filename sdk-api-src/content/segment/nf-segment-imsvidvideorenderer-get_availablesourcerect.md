---
UID: NF:segment.IMSVidVideoRenderer.get_AvailableSourceRect
title: IMSVidVideoRenderer::get_AvailableSourceRect (segment.h)
description: The get_AvailableSourceRect method retrieves the size of the native video.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_AvailableSourceRect method","IMSVidVideoRenderer.get_AvailableSourceRect","IMSVidVideoRenderer::get_AvailableSourceRect","IMSVidVideoRendererget_AvailableSourceRect","get_AvailableSourceRect","get_AvailableSourceRect method [Microsoft TV Technologies]","get_AvailableSourceRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_availablesourcerect","segment/IMSVidVideoRenderer::get_AvailableSourceRect"]
old-location: mstv\imsvidvideorenderer_get_availablesourcerect.htm
tech.root: mstv
ms.assetid: 33747e97-3e1c-4220-89c9-cc8310b77c4e
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_AvailableSourceRect method, IMSVidVideoRenderer.get_AvailableSourceRect, IMSVidVideoRenderer::get_AvailableSourceRect, IMSVidVideoRendererget_AvailableSourceRect, get_AvailableSourceRect, get_AvailableSourceRect method [Microsoft TV Technologies], get_AvailableSourceRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_availablesourcerect, segment/IMSVidVideoRenderer::get_AvailableSourceRect
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidVideoRenderer::get_AvailableSourceRect
 - segment/IMSVidVideoRenderer::get_AvailableSourceRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get_AvailableSourceRect
---

# IMSVidVideoRenderer::get_AvailableSourceRect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AvailableSourceRect</b> method retrieves the size of the native video.

## -parameters

### -param pRect [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The returned <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>