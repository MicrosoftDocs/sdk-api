---
UID: NF:msvidctl.IMSVidCtl.get_VideoRendererActive
title: IMSVidCtl::get_VideoRendererActive (msvidctl.h)
description: The get_VideoRendererActive method retrieves the currently active video renderer.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_VideoRendererActive method","IMSVidCtl.get_VideoRendererActive","IMSVidCtl::get_VideoRendererActive","IMSVidCtlget_VideoRendererActive","get_VideoRendererActive","get_VideoRendererActive method [Microsoft TV Technologies]","get_VideoRendererActive method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_videorendereractive","msvidctl/IMSVidCtl::get_VideoRendererActive"]
old-location: mstv\imsvidctl_get_videorendereractive.htm
tech.root: mstv
ms.assetid: 0b69abaf-95ab-49b9-9555-a2244224cb5d
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_VideoRendererActive method, IMSVidCtl.get_VideoRendererActive, IMSVidCtl::get_VideoRendererActive, IMSVidCtlget_VideoRendererActive, get_VideoRendererActive, get_VideoRendererActive method [Microsoft TV Technologies], get_VideoRendererActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_videorendereractive, msvidctl/IMSVidCtl::get_VideoRendererActive
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
 - IMSVidCtl::get_VideoRendererActive
 - msvidctl/IMSVidCtl::get_VideoRendererActive
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
 - IMSVidCtl.get_VideoRendererActive
---

# IMSVidCtl::get_VideoRendererActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_VideoRendererActive</b> method retrieves the currently active video renderer.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a> interface pointer.  The caller must release the interface. If no video renderer is active, this parameter receives the value <b>NULL</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_videorendereractive">IMSVidCtl::put_VideoRendererActive</a>