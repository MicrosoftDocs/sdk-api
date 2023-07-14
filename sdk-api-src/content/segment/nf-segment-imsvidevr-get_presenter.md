---
UID: NF:segment.IMSVidEVR.get_Presenter
title: IMSVidEVR::get_Presenter (segment.h)
description: .
helpviewer_keywords: ["IMSVidEVR interface [Microsoft TV Technologies]","get_Presenter method","IMSVidEVR.get_Presenter","IMSVidEVR::get_Presenter","IMSVidEVRget_Presenter","get_Presenter","get_Presenter method [Microsoft TV Technologies]","get_Presenter method [Microsoft TV Technologies]","IMSVidEVR interface","mstv.imsvidevr_get_presenter","segment/IMSVidEVR::get_Presenter"]
old-location: mstv\imsvidevr_get_presenter.htm
tech.root: mstv
ms.assetid: d3b5e272-8c71-4e84-b08f-b277eec643c4
ms.date: 12/05/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],get_Presenter method, IMSVidEVR.get_Presenter, IMSVidEVR::get_Presenter, IMSVidEVRget_Presenter, get_Presenter, get_Presenter method [Microsoft TV Technologies], get_Presenter method [Microsoft TV Technologies],IMSVidEVR interface, mstv.imsvidevr_get_presenter, segment/IMSVidEVR::get_Presenter
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IMSVidEVR::get_Presenter
 - segment/IMSVidEVR::get_Presenter
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
 - IMSVidEVR.get_Presenter
---

# IMSVidEVR::get_Presenter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Presenter</b> method retrieves the presenter object for the <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer</a> (EVR) filter.

## -parameters

### -param ppAllocPresent [out]

Receives a pointer to the <a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a> interface. This interface is documented in this Media Foundation SDK documentation. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidevr">IMSVidEVR</a>