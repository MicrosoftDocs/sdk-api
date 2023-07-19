---
UID: NF:segment.IMSVidEVR.put_Presenter
title: IMSVidEVR::put_Presenter (segment.h)
description: The put_Presenter method sets the presenter object for the Enhanced Video Renderer (EVR) filter.
helpviewer_keywords: ["IMSVidEVR interface [Microsoft TV Technologies]","put_Presenter method","IMSVidEVR.put_Presenter","IMSVidEVR::put_Presenter","IMSVidEVRput_Presenter","mstv.imsvidevr_put_presenter","put_Presenter","put_Presenter method [Microsoft TV Technologies]","put_Presenter method [Microsoft TV Technologies]","IMSVidEVR interface","segment/IMSVidEVR::put_Presenter"]
old-location: mstv\imsvidevr_put_presenter.htm
tech.root: mstv
ms.assetid: 602d92fc-e948-4cea-9bbf-8968c5e31257
ms.date: 12/05/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],put_Presenter method, IMSVidEVR.put_Presenter, IMSVidEVR::put_Presenter, IMSVidEVRput_Presenter, mstv.imsvidevr_put_presenter, put_Presenter, put_Presenter method [Microsoft TV Technologies], put_Presenter method [Microsoft TV Technologies],IMSVidEVR interface, segment/IMSVidEVR::put_Presenter
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
 - IMSVidEVR::put_Presenter
 - segment/IMSVidEVR::put_Presenter
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
 - IMSVidEVR.put_Presenter
---

# IMSVidEVR::put_Presenter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Presenter</b> method sets the presenter object for the <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer</a> (EVR) filter.

## -parameters

### -param pAllocPresent [in]

Pointer to a presenter's <a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a> interface. This interface is documented in this Media Foundation SDK documentation.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidevr">IMSVidEVR</a>