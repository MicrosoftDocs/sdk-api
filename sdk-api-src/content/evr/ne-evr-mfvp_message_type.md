---
UID: NE:evr.MFVP_MESSAGE_TYPE
title: MFVP_MESSAGE_TYPE (evr.h)
description: Defines messages for an enhanced video renderer (EVR) presenter.
helpviewer_keywords: ["71b92702-79a0-4c18-bb56-5e7c9e49cad2","MFVP_MESSAGE_BEGINSTREAMING","MFVP_MESSAGE_CANCELSTEP","MFVP_MESSAGE_ENDOFSTREAM","MFVP_MESSAGE_ENDSTREAMING","MFVP_MESSAGE_FLUSH","MFVP_MESSAGE_INVALIDATEMEDIATYPE","MFVP_MESSAGE_PROCESSINPUTNOTIFY","MFVP_MESSAGE_STEP","MFVP_MESSAGE_TYPE","MFVP_MESSAGE_TYPE enumeration [Media Foundation]","evr/MFVP_MESSAGE_BEGINSTREAMING","evr/MFVP_MESSAGE_CANCELSTEP","evr/MFVP_MESSAGE_ENDOFSTREAM","evr/MFVP_MESSAGE_ENDSTREAMING","evr/MFVP_MESSAGE_FLUSH","evr/MFVP_MESSAGE_INVALIDATEMEDIATYPE","evr/MFVP_MESSAGE_PROCESSINPUTNOTIFY","evr/MFVP_MESSAGE_STEP","evr/MFVP_MESSAGE_TYPE","mf.mfvp_message_type"]
old-location: mf\mfvp_message_type.htm
tech.root: mf
ms.assetid: 71b92702-79a0-4c18-bb56-5e7c9e49cad2
ms.date: 12/05/2018
ms.keywords: 71b92702-79a0-4c18-bb56-5e7c9e49cad2, MFVP_MESSAGE_BEGINSTREAMING, MFVP_MESSAGE_CANCELSTEP, MFVP_MESSAGE_ENDOFSTREAM, MFVP_MESSAGE_ENDSTREAMING, MFVP_MESSAGE_FLUSH, MFVP_MESSAGE_INVALIDATEMEDIATYPE, MFVP_MESSAGE_PROCESSINPUTNOTIFY, MFVP_MESSAGE_STEP, MFVP_MESSAGE_TYPE, MFVP_MESSAGE_TYPE enumeration [Media Foundation], evr/MFVP_MESSAGE_BEGINSTREAMING, evr/MFVP_MESSAGE_CANCELSTEP, evr/MFVP_MESSAGE_ENDOFSTREAM, evr/MFVP_MESSAGE_ENDSTREAMING, evr/MFVP_MESSAGE_FLUSH, evr/MFVP_MESSAGE_INVALIDATEMEDIATYPE, evr/MFVP_MESSAGE_PROCESSINPUTNOTIFY, evr/MFVP_MESSAGE_STEP, evr/MFVP_MESSAGE_TYPE, mf.mfvp_message_type
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVP_MESSAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFVP_MESSAGE_TYPE
 - evr/MFVP_MESSAGE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr.h
api_name:
 - MFVP_MESSAGE_TYPE
---

# MFVP_MESSAGE_TYPE enumeration


## -description

Defines messages for an enhanced video renderer (EVR) presenter. This enumeration is used with the <a href="/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage">IMFVideoPresenter::ProcessMessage</a> method.

## -enum-fields

### -field MFVP_MESSAGE_FLUSH:0

The presenter should discard any pending samples. The <i>ulParam</i> parameter is not used and should be zero.

### -field MFVP_MESSAGE_INVALIDATEMEDIATYPE:0x1

The mixer's output format has changed. The EVR will initiate format negotiation. The <i>ulParam</i> parameter is not used and should be zero.

### -field MFVP_MESSAGE_PROCESSINPUTNOTIFY:0x2

One input stream on the mixer has received a new sample. The <i>ulParam</i> parameter is not used and should be zero.

### -field MFVP_MESSAGE_BEGINSTREAMING:0x3

The EVR switched from stopped to paused. The presenter should allocate resources. The <i>ulParam</i> parameter is not used and should be zero.

### -field MFVP_MESSAGE_ENDSTREAMING:0x4

The EVR switched from running or paused to stopped. The presenter should free resources. The <i>ulParam</i> parameter is not used and should be zero.

### -field MFVP_MESSAGE_ENDOFSTREAM:0x5

All streams have ended. The <i>ulParam</i> parameter is not used and should be zero.

### -field MFVP_MESSAGE_STEP:0x6

Requests a frame step. The lower <b>DWORD</b> of the <i>ulParam</i> parameter contains the number of frames to step. If the value is <i>N</i>, the presenter should skip <i>N</i>–1 frames and display the <i>N</i>th frame. When that frame has been displayed, the presenter should send an <b>EC_STEP_COMPLETE</b> event to the EVR. If the presenter is not paused when it receives this message, it should return MF_E_INVALIDREQUEST.

### -field MFVP_MESSAGE_CANCELSTEP:0x7

Cancels a frame step. The <i>ulParam</i> parameter is not used and should be zero.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
