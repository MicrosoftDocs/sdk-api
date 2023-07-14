---
UID: NF:msvidctl.IMSVidCtl.get_VideoRenderersAvailable
title: IMSVidCtl::get_VideoRenderersAvailable (msvidctl.h)
description: The get_VideoRenderersAvailable method retrieves a collection of video renderers available on the local system.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_VideoRenderersAvailable method","IMSVidCtl.get_VideoRenderersAvailable","IMSVidCtl::get_VideoRenderersAvailable","IMSVidCtlget_VideoRenderersAvailable","get_VideoRenderersAvailable","get_VideoRenderersAvailable method [Microsoft TV Technologies]","get_VideoRenderersAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_videorenderersavailable","msvidctl/IMSVidCtl::get_VideoRenderersAvailable"]
old-location: mstv\imsvidctl_get_videorenderersavailable.htm
tech.root: mstv
ms.assetid: 20e5b2f3-33ea-4b0d-84b8-e4b0b61e0348
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_VideoRenderersAvailable method, IMSVidCtl.get_VideoRenderersAvailable, IMSVidCtl::get_VideoRenderersAvailable, IMSVidCtlget_VideoRenderersAvailable, get_VideoRenderersAvailable, get_VideoRenderersAvailable method [Microsoft TV Technologies], get_VideoRenderersAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_videorenderersavailable, msvidctl/IMSVidCtl::get_VideoRenderersAvailable
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - IMSVidCtl::get_VideoRenderersAvailable
 - msvidctl/IMSVidCtl::get_VideoRenderersAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_VideoRenderersAvailable
---

# IMSVidCtl::get_VideoRenderersAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_VideoRenderersAvailable</b> method retrieves a collection of video renderers available on the local system.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidvideorendererdevices">IMSVidVideoRendererDevices</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns a collection of video renderer devices. Use the returned <a href="/previous-versions/windows/desktop/mstv/msvidvideorendererdevices">IMSVidVideoRendererDevices</a> pointer to enumerate the collection.

<div class="alert"><b>Note</b>  In the current implementation, the collection always contains exactly one item: an <a href="/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object that represents the Video Mixing Renderer filter.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorendereractive">IMSVidCtl::get_VideoRendererActive</a>