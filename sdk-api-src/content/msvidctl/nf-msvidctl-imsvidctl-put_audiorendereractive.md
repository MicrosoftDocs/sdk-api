---
UID: NF:msvidctl.IMSVidCtl.put_AudioRendererActive
title: IMSVidCtl::put_AudioRendererActive (msvidctl.h)
description: The put_AudioRendererActive method specifies the active audio renderer.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_AudioRendererActive method","IMSVidCtl.put_AudioRendererActive","IMSVidCtl::put_AudioRendererActive","IMSVidCtlput_AudioRendererActive","mstv.imsvidctl_put_audiorendereractive","msvidctl/IMSVidCtl::put_AudioRendererActive","put_AudioRendererActive","put_AudioRendererActive method [Microsoft TV Technologies]","put_AudioRendererActive method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_audiorendereractive.htm
tech.root: mstv
ms.assetid: 1f6498ce-fb53-4d57-b6bd-6696ba57de3b
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_AudioRendererActive method, IMSVidCtl.put_AudioRendererActive, IMSVidCtl::put_AudioRendererActive, IMSVidCtlput_AudioRendererActive, mstv.imsvidctl_put_audiorendereractive, msvidctl/IMSVidCtl::put_AudioRendererActive, put_AudioRendererActive, put_AudioRendererActive method [Microsoft TV Technologies], put_AudioRendererActive method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_AudioRendererActive
 - msvidctl/IMSVidCtl::put_AudioRendererActive
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
 - IMSVidCtl.put_AudioRendererActive
---

# IMSVidCtl::put_AudioRendererActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_AudioRendererActive</b> method specifies the active audio renderer.

## -parameters

### -param pVal [in]

Pointer to an <a href="/previous-versions/windows/desktop/mstv/msvidaudiorenderer">IMSVidAudioRenderer</a> interface that specifies the audio renderer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">IMSVidCtl::get_AudioRendererActive</a>