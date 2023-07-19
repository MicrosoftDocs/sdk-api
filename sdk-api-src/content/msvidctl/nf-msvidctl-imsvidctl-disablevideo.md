---
UID: NF:msvidctl.IMSVidCtl.DisableVideo
title: IMSVidCtl::DisableVideo (msvidctl.h)
description: The DisableVideo method disables the video renderer.
helpviewer_keywords: ["DisableVideo","DisableVideo method [Microsoft TV Technologies]","DisableVideo method [Microsoft TV Technologies]","IMSVidCtl interface","IMSVidCtl interface [Microsoft TV Technologies]","DisableVideo method","IMSVidCtl.DisableVideo","IMSVidCtl::DisableVideo","IMSVidCtlDisableVideo","mstv.imsvidctl_disablevideo","msvidctl/IMSVidCtl::DisableVideo"]
old-location: mstv\imsvidctl_disablevideo.htm
tech.root: mstv
ms.assetid: 5c8f7af1-0416-4860-aa05-d2167452291e
ms.date: 12/05/2018
ms.keywords: DisableVideo, DisableVideo method [Microsoft TV Technologies], DisableVideo method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],DisableVideo method, IMSVidCtl.DisableVideo, IMSVidCtl::DisableVideo, IMSVidCtlDisableVideo, mstv.imsvidctl_disablevideo, msvidctl/IMSVidCtl::DisableVideo
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
 - IMSVidCtl::DisableVideo
 - msvidctl/IMSVidCtl::DisableVideo
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
 - IMSVidCtl.DisableVideo
---

# IMSVidCtl::DisableVideo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>DisableVideo</b> method disables the video renderer.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method sets the active video renderer device to <b>NULL</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_videorendereractive">IMSVidCtl::put_VideoRendererActive</a>
