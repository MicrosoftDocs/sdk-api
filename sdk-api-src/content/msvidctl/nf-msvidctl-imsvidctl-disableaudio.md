---
UID: NF:msvidctl.IMSVidCtl.DisableAudio
title: IMSVidCtl::DisableAudio (msvidctl.h)
description: The DisableAudio method disables the audio output device.
helpviewer_keywords: ["DisableAudio","DisableAudio method [Microsoft TV Technologies]","DisableAudio method [Microsoft TV Technologies]","IMSVidCtl interface","IMSVidCtl interface [Microsoft TV Technologies]","DisableAudio method","IMSVidCtl.DisableAudio","IMSVidCtl::DisableAudio","IMSVidCtlDisableAudio","mstv.imsvidctl_disableaudio","msvidctl/IMSVidCtl::DisableAudio"]
old-location: mstv\imsvidctl_disableaudio.htm
tech.root: mstv
ms.assetid: 0166cdc3-de1c-4505-855e-f69144cc71aa
ms.date: 12/05/2018
ms.keywords: DisableAudio, DisableAudio method [Microsoft TV Technologies], DisableAudio method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],DisableAudio method, IMSVidCtl.DisableAudio, IMSVidCtl::DisableAudio, IMSVidCtlDisableAudio, mstv.imsvidctl_disableaudio, msvidctl/IMSVidCtl::DisableAudio
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
 - IMSVidCtl::DisableAudio
 - msvidctl/IMSVidCtl::DisableAudio
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
 - IMSVidCtl.DisableAudio
---

# IMSVidCtl::DisableAudio


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>DisableAudio</b> method disables the audio output device.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method sets the active audio output device to <b>NULL</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_audiorendereractive">IMSVidCtl::put_AudioRendererActive</a>
