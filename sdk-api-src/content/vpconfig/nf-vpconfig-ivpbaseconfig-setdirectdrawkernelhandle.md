---
UID: NF:vpconfig.IVPBaseConfig.SetDirectDrawKernelHandle
title: IVPBaseConfig::SetDirectDrawKernelHandle (vpconfig.h)
description: The SetDirectDrawKernelHandle method sets the kernel-mode handle to the DirectDraw object. This handle enables the device's mini-driver to communicate with DirectDraw.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetDirectDrawKernelHandle method","IVPBaseConfig.SetDirectDrawKernelHandle","IVPBaseConfig::SetDirectDrawKernelHandle","IVPBaseConfigSetDirectDrawKernelHandle","SetDirectDrawKernelHandle","SetDirectDrawKernelHandle method [DirectShow]","SetDirectDrawKernelHandle method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setdirectdrawkernelhandle","vpconfig/IVPBaseConfig::SetDirectDrawKernelHandle"]
old-location: dshow\ivpbaseconfig_setdirectdrawkernelhandle.htm
tech.root: dshow
ms.assetid: f3a04341-6cca-4fb4-bf47-30659d039a0d
ms.date: 4/26/2023
ms.keywords: IVPBaseConfig interface [DirectShow],SetDirectDrawKernelHandle method, IVPBaseConfig.SetDirectDrawKernelHandle, IVPBaseConfig::SetDirectDrawKernelHandle, IVPBaseConfigSetDirectDrawKernelHandle, SetDirectDrawKernelHandle, SetDirectDrawKernelHandle method [DirectShow], SetDirectDrawKernelHandle method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setdirectdrawkernelhandle, vpconfig/IVPBaseConfig::SetDirectDrawKernelHandle
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IVPBaseConfig::SetDirectDrawKernelHandle
 - vpconfig/IVPBaseConfig::SetDirectDrawKernelHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetDirectDrawKernelHandle
---

# IVPBaseConfig::SetDirectDrawKernelHandle


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDirectDrawKernelHandle</code> method sets the kernel-mode handle to the DirectDraw object. This handle enables the device's mini-driver to communicate with DirectDraw.

## -parameters

### -param dwDDKernelHandle [in]

Specifies the kernel-mode handle of the DirectDraw object.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>