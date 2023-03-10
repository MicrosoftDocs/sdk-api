---
UID: NE:strmif.tagVideoProcAmpFlags
title: VideoProcAmpFlags (strmif.h)
description: The VideoProcAmpFlags enumeration indicates whether a particular video property is controlled manually or automatically.
helpviewer_keywords: ["VideoProcAmpFlags","VideoProcAmpFlags enumeration [DirectShow]","VideoProcAmpFlagsEnumeration","VideoProcAmp_Flags_Auto","VideoProcAmp_Flags_Manual","dshow.videoprocampflags","strmif/VideoProcAmpFlags","strmif/VideoProcAmp_Flags_Auto","strmif/VideoProcAmp_Flags_Manual"]
old-location: dshow\videoprocampflags.htm
tech.root: dshow
ms.assetid: 42876f3b-d2b9-4ddb-85c0-80f5177eef6b
ms.date: 12/05/2018
ms.keywords: VideoProcAmpFlags, VideoProcAmpFlags enumeration [DirectShow], VideoProcAmpFlagsEnumeration, VideoProcAmp_Flags_Auto, VideoProcAmp_Flags_Manual, dshow.videoprocampflags, strmif/VideoProcAmpFlags, strmif/VideoProcAmp_Flags_Auto, strmif/VideoProcAmp_Flags_Manual
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
req.typenames: VideoProcAmpFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVideoProcAmpFlags
 - strmif/tagVideoProcAmpFlags
 - VideoProcAmpFlags
 - strmif/VideoProcAmpFlags
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
 - VideoProcAmpFlags
---

# VideoProcAmpFlags enumeration


## -description

The <b>VideoProcAmpFlags</b> enumeration indicates whether a particular video property is controlled manually or automatically.

## -enum-fields

### -field VideoProcAmp_Flags_Auto:0x1

The setting is controlled automatically.

### -field VideoProcAmp_Flags_Manual:0x2

The setting is controlled manually.

## -remarks

The following flags defined in KsMedia.h are equivalent to the values in <b>VideoProcAmpFlags</b>:


``` syntax
#define KSPROPERTY_VIDEOPROCAMP_FLAGS_AUTO        0X0001L
#define KSPROPERTY_VIDEOPROCAMP_FLAGS_MANUAL      0X0002L
```


## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>
