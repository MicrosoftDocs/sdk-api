---
UID: NF:msvidctl.IMSVidCtl.put_VideoRendererActive
title: IMSVidCtl::put_VideoRendererActive (msvidctl.h)
description: The put_VideoRendererActive method specifies the active video renderer.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_VideoRendererActive method","IMSVidCtl.put_VideoRendererActive","IMSVidCtl::put_VideoRendererActive","IMSVidCtlput_VideoRendererActive","mstv.imsvidctl_put_videorendereractive","msvidctl/IMSVidCtl::put_VideoRendererActive","put_VideoRendererActive","put_VideoRendererActive method [Microsoft TV Technologies]","put_VideoRendererActive method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_videorendereractive.htm
tech.root: mstv
ms.assetid: fb6e1db7-b980-4706-a1f1-cd6d8423bfb2
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_VideoRendererActive method, IMSVidCtl.put_VideoRendererActive, IMSVidCtl::put_VideoRendererActive, IMSVidCtlput_VideoRendererActive, mstv.imsvidctl_put_videorendereractive, msvidctl/IMSVidCtl::put_VideoRendererActive, put_VideoRendererActive, put_VideoRendererActive method [Microsoft TV Technologies], put_VideoRendererActive method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_VideoRendererActive
 - msvidctl/IMSVidCtl::put_VideoRendererActive
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
 - IMSVidCtl.put_VideoRendererActive
---

# IMSVidCtl::put_VideoRendererActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_VideoRendererActive</b> method specifies the active video renderer.

## -parameters

### -param pVal [in]

Specifies a pointer to the <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a> interface of the video renderer device.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Currently the only supported video renderer is the Video Mixing Renderer (VMR) filter. The VMR is used by default, so it is not necessary to call this method.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorendereractive">IMSVidCtl::get_VideoRendererActive</a>