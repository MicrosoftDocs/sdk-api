---
UID: NF:strmif.IVMRVideoStreamControl.GetStreamActiveState
title: IVMRVideoStreamControl::GetStreamActiveState (strmif.h)
description: The GetStreamActiveState method retrieves the state of the stream.
helpviewer_keywords: ["GetStreamActiveState","GetStreamActiveState method [DirectShow]","GetStreamActiveState method [DirectShow]","IVMRVideoStreamControl interface","IVMRVideoStreamControl interface [DirectShow]","GetStreamActiveState method","IVMRVideoStreamControl.GetStreamActiveState","IVMRVideoStreamControl::GetStreamActiveState","IVMRVideoStreamControlGetStreamActiveState","dshow.ivmrvideostreamcontrol_getstreamactivestate","strmif/IVMRVideoStreamControl::GetStreamActiveState"]
old-location: dshow\ivmrvideostreamcontrol_getstreamactivestate.htm
tech.root: dshow
ms.assetid: 619ba669-c2a0-46fe-9c12-52105b107351
ms.date: 12/05/2018
ms.keywords: GetStreamActiveState, GetStreamActiveState method [DirectShow], GetStreamActiveState method [DirectShow],IVMRVideoStreamControl interface, IVMRVideoStreamControl interface [DirectShow],GetStreamActiveState method, IVMRVideoStreamControl.GetStreamActiveState, IVMRVideoStreamControl::GetStreamActiveState, IVMRVideoStreamControlGetStreamActiveState, dshow.ivmrvideostreamcontrol_getstreamactivestate, strmif/IVMRVideoStreamControl::GetStreamActiveState
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRVideoStreamControl::GetStreamActiveState
 - strmif/IVMRVideoStreamControl::GetStreamActiveState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRVideoStreamControl.GetStreamActiveState
---

# IVMRVideoStreamControl::GetStreamActiveState


## -description

The <code>GetStreamActiveState</code> method retrieves the state of the stream.

## -parameters

### -param lpfActive [out]

Receives the current state of the stream. <b>TRUE</b> means the stream is active; <b>FALSE</b> means that it is inactive.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrvideostreamcontrol">IVMRVideoStreamControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate">IVMRVideoStreamControl::SetStreamActiveState</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>