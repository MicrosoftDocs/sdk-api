---
UID: NF:msvidctl.IMSVidCtl.get_AudioRenderersAvailable
title: IMSVidCtl::get_AudioRenderersAvailable (msvidctl.h)
description: The get_AudioRenderersAvailable method retrieves the available audio renderers.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_AudioRenderersAvailable method","IMSVidCtl.get_AudioRenderersAvailable","IMSVidCtl::get_AudioRenderersAvailable","IMSVidCtlget_AudioRenderersAvailable","get_AudioRenderersAvailable","get_AudioRenderersAvailable method [Microsoft TV Technologies]","get_AudioRenderersAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_audiorenderersavailable","msvidctl/IMSVidCtl::get_AudioRenderersAvailable"]
old-location: mstv\imsvidctl_get_audiorenderersavailable.htm
tech.root: mstv
ms.assetid: 6ab81536-2701-408e-be3a-f44375ef8193
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_AudioRenderersAvailable method, IMSVidCtl.get_AudioRenderersAvailable, IMSVidCtl::get_AudioRenderersAvailable, IMSVidCtlget_AudioRenderersAvailable, get_AudioRenderersAvailable, get_AudioRenderersAvailable method [Microsoft TV Technologies], get_AudioRenderersAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_audiorenderersavailable, msvidctl/IMSVidCtl::get_AudioRenderersAvailable
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
 - IMSVidCtl::get_AudioRenderersAvailable
 - msvidctl/IMSVidCtl::get_AudioRenderersAvailable
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
 - IMSVidCtl.get_AudioRenderersAvailable
---

# IMSVidCtl::get_AudioRenderersAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AudioRenderersAvailable</b> method retrieves the available audio renderers.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidaudiorendererdevices">IMSVidAudioRendererDevices</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns a read-only collection of input devices. Use the returned <a href="/previous-versions/windows/desktop/mstv/msvidaudiorendererdevices">IMSVidAudioRendererDevices</a> pointer to enumerate the collection.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorendereractive">IMSVidCtl::get_AudioRendererActive</a>