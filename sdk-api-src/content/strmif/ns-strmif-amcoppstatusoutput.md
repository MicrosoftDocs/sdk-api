---
UID: NS:strmif._AMCOPPStatusOutput
title: AMCOPPStatusOutput (strmif.h)
description: The AMCOPPStatusOutput structure contains the result of a Certified Output Protection Protocol (COPP) status request.
helpviewer_keywords: ["*LPAMCOPPStatusOutput","AMCOPPStatusOutput","AMCOPPStatusOutput structure [DirectShow]","AMCOPPStatusOutputStructure","LPAMCOPPStatusOutput","LPAMCOPPStatusOutput structure pointer [DirectShow]","dshow.amcoppstatusoutput","strmif/AMCOPPStatusOutput","strmif/LPAMCOPPStatusOutput"]
old-location: dshow\amcoppstatusoutput.htm
tech.root: dshow
ms.assetid: 136ce182-24c3-489d-a9c2-0121593e4b1e
ms.date: 4/26/2023
ms.keywords: '*LPAMCOPPStatusOutput, AMCOPPStatusOutput, AMCOPPStatusOutput structure [DirectShow], AMCOPPStatusOutputStructure, LPAMCOPPStatusOutput, LPAMCOPPStatusOutput structure pointer [DirectShow], dshow.amcoppstatusoutput, strmif/AMCOPPStatusOutput, strmif/LPAMCOPPStatusOutput'
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: AMCOPPStatusOutput, *LPAMCOPPStatusOutput
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMCOPPStatusOutput
 - strmif/_AMCOPPStatusOutput
 - LPAMCOPPStatusOutput
 - strmif/LPAMCOPPStatusOutput
 - AMCOPPStatusOutput
 - strmif/AMCOPPStatusOutput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AMCOPPStatusOutput
---

# AMCOPPStatusOutput structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMCOPPStatusOutput</b> structure contains the result of a Certified Output Protection Protocol (COPP) status request.

## -struct-fields

### -field macKDI

Message Authentication Code (MAC) of the status data. The driver will use AES-based one-key CBC MAC (OMAC) to calculate this value.

### -field cbSizeData

Size of the valid data in the <b>COPPStatus</b> member.

### -field COPPStatus

Buffer that contains the result of the status request.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>