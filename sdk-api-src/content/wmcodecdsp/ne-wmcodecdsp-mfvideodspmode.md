---
UID: NE:wmcodecdsp._MFVideoDSPMode
title: MFVideoDSPMode (wmcodecdsp.h)
description: Specifies the processing mode of the Video Stabilization MFT.
helpviewer_keywords: ["MFVideoDSPMode","MFVideoDSPMode enumeration [Media Foundation]","MFVideoDSPMode_Passthrough","MFVideoDSPMode_Stabilization","mf.mfvideodspmode","wmcodecdsp/MFVideoDSPMode","wmcodecdsp/MFVideoDSPMode_Passthrough","wmcodecdsp/MFVideoDSPMode_Stabilization"]
old-location: mf\mfvideodspmode.htm
tech.root: mf
ms.assetid: 24A5190B-6839-4CA1-ADBF-CDBF9B47C6AF
ms.date: 12/05/2018
ms.keywords: MFVideoDSPMode, MFVideoDSPMode enumeration [Media Foundation], MFVideoDSPMode_Passthrough, MFVideoDSPMode_Stabilization, mf.mfvideodspmode, wmcodecdsp/MFVideoDSPMode, wmcodecdsp/MFVideoDSPMode_Passthrough, wmcodecdsp/MFVideoDSPMode_Stabilization
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MFVideoDSPMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoDSPMode
 - wmcodecdsp/_MFVideoDSPMode
 - MFVideoDSPMode
 - wmcodecdsp/MFVideoDSPMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - MFVideoDSPMode
---

# MFVideoDSPMode enumeration


## -description

Specifies the processing mode of the <a href="/windows/desktop/medfound/video-stabilization-mft">Video Stabilization MFT</a>.

## -enum-fields

### -field MFVideoDSPMode_Passthrough:1

Pass-through mode. Video stabilization is not applied.

### -field MFVideoDSPMode_Stabilization:4

Video stabilization is applied.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-videodsp-mode">MF_VIDEODSP_MODE</a> attribute.

In pass-through mode, the MFT does not apply any processing to the video.

## -see-also

<a href="/windows/desktop/medfound/mf-videodsp-mode">MF_VIDEODSP_MODE</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/video-stabilization-mft">Video Stabilization MFT</a>
