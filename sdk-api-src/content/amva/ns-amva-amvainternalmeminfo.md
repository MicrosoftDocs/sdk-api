---
UID: NS:amva._tag_AMVAInternalMemInfo
title: AMVAInternalMemInfo (amva.h)
description: The AMVAInternalMemInfo structure specifies the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use.
helpviewer_keywords: ["*LPAMVAInternalMemInfo","AMVAInternalMemInfo","AMVAInternalMemInfo structure [DirectShow]","AMVAInternalMemInfoStructure","LPAMVAInternalMemInfo","LPAMVAInternalMemInfo structure pointer [DirectShow]","amva/AMVAInternalMemInfo","amva/LPAMVAInternalMemInfo","dshow.amvainternalmeminfo"]
old-location: dshow\amvainternalmeminfo.htm
tech.root: dshow
ms.assetid: 8ce27daa-cd8e-4dbd-a949-0c07c370d504
ms.date: 12/05/2018
ms.keywords: '*LPAMVAInternalMemInfo, AMVAInternalMemInfo, AMVAInternalMemInfo structure [DirectShow], AMVAInternalMemInfoStructure, LPAMVAInternalMemInfo, LPAMVAInternalMemInfo structure pointer [DirectShow], amva/AMVAInternalMemInfo, amva/LPAMVAInternalMemInfo, dshow.amvainternalmeminfo'
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
req.typenames: AMVAInternalMemInfo, *LPAMVAInternalMemInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVAInternalMemInfo
 - amva/_tag_AMVAInternalMemInfo
 - LPAMVAInternalMemInfo
 - amva/LPAMVAInternalMemInfo
 - AMVAInternalMemInfo
 - amva/AMVAInternalMemInfo
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
 - AMVAInternalMemInfo
---

# AMVAInternalMemInfo structure


## -description

The <b>AMVAInternalMemInfo</b> structure specifies the amount of scratch memory the hardware abstraction layer (HAL) will allocate for its private use.

## -struct-fields

### -field dwScratchMemAlloc

Amount of scratch memory the HAL will allocate for its private use.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getinternalmeminfo">IAMVideoAccelerator::GetInternalMemInfo</a>