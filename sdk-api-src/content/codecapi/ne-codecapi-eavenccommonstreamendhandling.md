---
UID: NE:codecapi.eAVEncCommonStreamEndHandling
title: eAVEncCommonStreamEndHandling (codecapi.h)
description: Specifies whether the encoder discards partial groups of pictures (GOPs) at the end of the stream. This enumeration is used with the AVEncCommonStreamEndHandling codec property.
helpviewer_keywords: ["codecapi/eAVEncCommonStreamEndHandling","codecapi/eAVEncCommonStreamEndHandling_DiscardPartial","codecapi/eAVEncCommonStreamEndHandling_EnsureComplete","dshow.eavenccommonstreamendhandling","eAVEncCommonStreamEndHandling","eAVEncCommonStreamEndHandling enumeration [DirectShow]","eAVEncCommonStreamEndHandlingEnumeration","eAVEncCommonStreamEndHandling_DiscardPartial","eAVEncCommonStreamEndHandling_EnsureComplete"]
old-location: dshow\eavenccommonstreamendhandling.htm
tech.root: dshow
ms.assetid: 406dbfe6-d5c8-44b1-9052-88df40a6a522
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncCommonStreamEndHandling, codecapi/eAVEncCommonStreamEndHandling_DiscardPartial, codecapi/eAVEncCommonStreamEndHandling_EnsureComplete, dshow.eavenccommonstreamendhandling, eAVEncCommonStreamEndHandling, eAVEncCommonStreamEndHandling enumeration [DirectShow], eAVEncCommonStreamEndHandlingEnumeration, eAVEncCommonStreamEndHandling_DiscardPartial, eAVEncCommonStreamEndHandling_EnsureComplete
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - eAVEncCommonStreamEndHandling
 - codecapi/eAVEncCommonStreamEndHandling
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncCommonStreamEndHandling
---

# eAVEncCommonStreamEndHandling enumeration


## -description

Specifies whether the encoder discards partial groups of pictures (GOPs) at the end of the stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avenccommonstreamendhandling-property">AVEncCommonStreamEndHandling</a> codec property.

## -enum-fields

### -field eAVEncCommonStreamEndHandling_DiscardPartial:0

If there is a partial GOP at the end of the stream, the encoder will discard it.

### -field eAVEncCommonStreamEndHandling_EnsureComplete:1

If there is a partial GOP at the end of the stream, the encoder will adjust the GOP and encode all of the stream data.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
