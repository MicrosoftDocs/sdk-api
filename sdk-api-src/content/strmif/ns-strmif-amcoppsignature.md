---
UID: NS:strmif._AMCOPPSignature
title: AMCOPPSignature (strmif.h)
description: The AMCOPPSignature structure contains the signature needed for the IAMCertifiedOutputProtection::SessionSequenceStart method.
helpviewer_keywords: ["AMCOPPSignature","AMCOPPSignature structure [DirectShow]","AMCOPPSignatureStructure","dshow.amcoppsignature","strmif/AMCOPPSignature"]
old-location: dshow\amcoppsignature.htm
tech.root: dshow
ms.assetid: eaf220cf-111f-42fa-80db-1c69cd863258
ms.date: 4/26/2023
ms.keywords: AMCOPPSignature, AMCOPPSignature structure [DirectShow], AMCOPPSignatureStructure, dshow.amcoppsignature, strmif/AMCOPPSignature
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
req.typenames: AMCOPPSignature
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMCOPPSignature
 - strmif/_AMCOPPSignature
 - AMCOPPSignature
 - strmif/AMCOPPSignature
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
 - AMCOPPSignature
---

# AMCOPPSignature structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMCOPPSignature</b> structure contains the signature needed for the <a href="/windows/desktop/api/strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart">IAMCertifiedOutputProtection::SessionSequenceStart</a> method.

## -struct-fields

### -field Signature

Buffer that contains the signature. For more information, see the Remarks section for the <b>SessionSequenceStart</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>