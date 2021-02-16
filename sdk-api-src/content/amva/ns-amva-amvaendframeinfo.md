---
UID: NS:amva._tag_AMVAEndFrameInfo
title: AMVAEndFrameInfo (amva.h)
description: The AMVAEndFrameInfo structure contains information for the IAMVideoAccelerator::EndFrame method.
helpviewer_keywords: ["*LPAMVAEndFrameInfo","AMVAEndFrameInfo","AMVAEndFrameInfo structure [DirectShow]","AMVAEndFrameInfoStructure","LPAMVAEndFrameInfo","LPAMVAEndFrameInfo structure pointer [DirectShow]","amva/AMVAEndFrameInfo","amva/LPAMVAEndFrameInfo","dshow.amvaendframeinfo"]
old-location: dshow\amvaendframeinfo.htm
tech.root: dshow
ms.assetid: 7f9308c1-0426-4c0f-97aa-4d946ac2403a
ms.date: 12/05/2018
ms.keywords: '*LPAMVAEndFrameInfo, AMVAEndFrameInfo, AMVAEndFrameInfo structure [DirectShow], AMVAEndFrameInfoStructure, LPAMVAEndFrameInfo, LPAMVAEndFrameInfo structure pointer [DirectShow], amva/AMVAEndFrameInfo, amva/LPAMVAEndFrameInfo, dshow.amvaendframeinfo'
req.header: amva.h
req.include-header: Videoacc.h
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
req.typenames: AMVAEndFrameInfo, *LPAMVAEndFrameInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVAEndFrameInfo
 - amva/_tag_AMVAEndFrameInfo
 - LPAMVAEndFrameInfo
 - amva/LPAMVAEndFrameInfo
 - AMVAEndFrameInfo
 - amva/AMVAEndFrameInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amva.h
api_name:
 - AMVAEndFrameInfo
---

# AMVAEndFrameInfo structure


## -description

The <b>AMVAEndFrameInfo</b> structure contains information  for the <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe">IAMVideoAccelerator::EndFrame</a> method.

## -struct-fields

### -field dwSizeMiscData

Size, in bytes, of the buffer that <b>pMiscData</b> points to. The value must be 2.

### -field pMiscData

Pointer to a buffer that contains data for the video accelerator.

This buffer must contain a <b>WORD</b> value equal equal to the same surface index that passed to the corresponding <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe">IAMVideoAccelerator::BeginFrame</a> method.

## -remarks

The buffer pointed to by <b>pMiscData</b> cannot contain pointer values, because their addresses will not be valid in kernel mode, where frame processing occurs.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe">IAMVideoAccelerator::EndFrame</a>